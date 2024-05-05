<script>
  let quizData;

  async function fetchQuizData() {
    const response = await fetch(
      "https://raw.githubusercontent.com/kembak/multisvelte-json/main/quiz.json"
    );
    quizData = await response.json();
  }

  fetchQuizData();

  let currentQuestionIndex = 0;
  let numCorrectAnswers = 0;
  let answer;

  function submitAnswer(answer) {
    if (answer === quizData[currentQuestionIndex].correctAnswer) {
      numCorrectAnswers++;
    }
    currentQuestionIndex++;
  }

  function finishQuiz() {
    // Display number of correct answers and reset quiz
    alert(`You got ${numCorrectAnswers} out of ${quizData.length} correct.`);
    currentQuestionIndex = 0;
    numCorrectAnswers = 0;
    answer = "";
  }
</script>

<br><br>

{#if quizData}
  {#if currentQuestionIndex < quizData.length}
    <!-- Display current question -->
    <div class="quizkont">
      <h2>{quizData[currentQuestionIndex].question}</h2>
      {#if quizData[currentQuestionIndex].type === "text"}
        <div class="inputsvar">
        <input type="text" bind:value={answer} />
        <button on:click={() => submitAnswer(answer)}>SVAR</button>
        </div>
      {:else if quizData[currentQuestionIndex].type === "button"}
        {#each quizData[currentQuestionIndex].answers as option}
          <div class="columnar">
            <button class="svaralternativ" on:click={() => submitAnswer(option)}
              >{option}</button
            >
          </div>
        {/each}
      {/if}
    </div>
  {:else}
    <!-- Display finish quiz button -->
    <div class="quizkont">
    <div class="columnar">
      <button class="svaralternativ" style="margin-top: 10rem; width: 30%" on:click={finishQuiz}>Avslutt Quiz</button>
    </div>
    </div>
  {/if}
{/if}

<style>
  .quizkont {
    padding: 3rem;
    font-family: garamond;
    min-height: 60vh;
    color: black;
  }
  .quizkont h2 {
    color: white;
    text-transform: uppercase;
    font-size: xx-large;
  }
  .svaralternativ {
    display: block;
    width: 50%;
    color: black;
    background-color: #ffcc66;
    font-size: larger;
    margin: 0.5rem 0 0.5rem 0;
    padding: 0.75rem;
    border: 0px solid white;
    border-radius: 2rem;
    transition: 0.1s ease;
  }
  .svaralternativ:hover, .inputsvar button:hover {
    background-color: white;
    box-shadow: 0 0 .5rem rgba(0, 0, 0, 0.5);
  }
  .inputsvar{
    width: 60%;
    margin: 6rem auto;
    display: flex;
    justify-content: space-between;
  }
  .inputsvar button{
    all: unset;
    font-family: Arial, Helvetica, sans-serif;
    font-size: larger;
    text-align: center;
    width: 8rem;
    background-color: #ffcc66;
    color: black;
    border-radius: 2rem;
    transition: 0.1s ease;
  }
  .inputsvar input{
    all: unset;
    text-align: center;
    font-family: Arial, Helvetica, sans-serif;
    background-color: white;
    width: 100%;
    margin-right: 1rem;
    font-size: larger;
    padding: .75rem;
    border: none;
    border-radius: 2rem;
  }
  .inputsvar input:focus, input:hover{
    box-shadow: 0 0 .5rem rgba(0, 0, 0, 0.5);
  }
</style>
