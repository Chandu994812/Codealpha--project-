# Codealpha--project-
Projects of codealpha 
# Code-alpha
// Codealpha projects
// fitness tracker 

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fitness Tracker</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
      color: #333;
    }

    header {
      background-color: #007bff;
      color: ## Code-alpha
// Codealpha projects
// fitness tracker 

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fitness Tracker</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
      color: #333;
    }

    header {
      background-color: #007bff;
      color: #fff;
      padding: 20px;
      text-align: center;
    }

    main {
      padding: 20px;
    }

    section {
      margin-bottom: 20px;
    }

    h2 {
      color: #007bff;
    }

    form {
      display: flex;
      flex-direction: column;
      max-width: 300px;
    }

    label {
      margin-bottom: 5px;
    }

    input[type="number"] {
      padding: 5px;
      margin-bottom: 10px;
    }

    button {
      background-color: #007bff;
      color: #fff;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
    }

    button:hover {
      background-color: #0056b3;
    }

    #progress-chart {
      height: 300px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Fitness Tracker</h1>
  </header>
  <main>
    <section id="workout-form">
      <h2>Add Workout</h2>
      <form id="workout-form">
        <label for="exercise-type">Exercise Type:</label>
        <select id="exercise-type">
          <option value="cardio">Cardio</option>
          <option value="strength">Strength Training</option>
          <option value="flexibility">Flexibility</option>
        </select>
        <label for="duration">Duration (minutes):</label>
        <input type="number" id="duration" min="1" required>
        <button type="submit">Add Workout</button>
      </form>
    </section>
    <section id="goals">
      <h2>Set Goals</h2>
      <form id="goals-form">
        <label for="goal">Daily Exercise Goal (minutes):</label>
        <input type="number" id="goal" min="1" required>
        <button type="submit">Set Goal</button>
      </form>
    </section>
    <section id="progress">
      <h2>Progress</h2>
      <div id="progress-chart"></div>
    </section>
  </main>
  <script>
    // Get form elements
    const workoutForm = document.getElementById('workout-form');
    const goalsForm = document.getElementById('goals-form');

    // Add event listeners
    workoutForm.addEventListener('submit', addWorkout);
    goalsForm.addEventListener('submit', setGoal);

    // Function to add workout
    function addWorkout(event) {
      event.preventDefault();
      const exerciseType = document.getElementById('exercise-type').value;
      const duration = parseInt(document.getElementById('duration').value);
      // Add workout to the progress chart
      // This is a placeholder for a real charting library or implementation
      console.log(`Added ${duration} minutes of ${exerciseType} workout.`);
      // You can update the progress chart here
    }

    // Function to set goal
    function setGoal(event) {
      event.preventDefault();
      const goal = parseInt(document.getElementById('goal').value);
      // Store goal in local storage or send it to server
      console.log(`Set daily exercise goal to ${goal} minutes.`);
    }
  </script>
</body>
</html>





// Random quote generator app





<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Quote Generator</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      font-family: Verdana, Geneva, Tahoma, sans-serif;
      box-sizing: border-box;
      line-height: 30px;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      margin: 0 1rem;
      min-height: 100vh;
      text-align: center;
      background: rgb(131, 58, 180);
      background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 41%, rgba(252, 176, 69, 1) 100%);
    }

    .main-content {
      background-color: #e1e1e1;
      padding: 5rem;
      margin-top: 2rem;
      border-radius: 5px;
      text-align: center;
    }

    .container {
      max-width: 768px;
    }

    h1 {
      color: #fff;
    }

    .main-content .quote {
      font-family: 'Times New Roman', Times, serif;
      font-size: 20px;
    }

    .main-content .quote::before {
      content: "“";
      font-size: 20px;
      color: blue;
      font-weight: bold;
      margin-right: 5px;
      opacity: 0.6;
    }

    .main-content .quote::after {
      content: "”";
      font-size: 20px;
      color: blue;
      font-weight: bold;
      margin-left: 5px;
      align-items: center;
    }

    .main-content .person {
      margin-top: 30px;
      font-weight: bold;
      max-width: 100px;
    }

    button {
      padding: 0.75rem 2rem;
      margin-top: 15px;
      background: rgb(131, 58, 180);
      background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 41%, rgba(252, 176, 69, 1) 100%);
      outline: none;
      border: none;
      color: #fff;
      font-weight: bold;
      letter-spacing: 1px;
      border-radius: 4px;
    }

    .quote-container {
      margin-bottom: 15px;
    }
  </style>
</head>
<body>
  <h1>Quote Generator</h1>
  <div class="main-content">
    <div class="quote-container">
      <span class="quote">
        The only way to do great work is to love what you do.
      </span>
    </div>
    <span class="person">
      Steve Jobs
    </span>
  </div>

  <div>
    <button type="button" title="Next Quote" id="nextQuote">Next Quote</button>
  </div>

  <script>
    let quote = document.querySelector(".quote");
    let person = document.querySelector(".person");
    let btn = document.getElementById("nextQuote");

    const quotesData = {
      quotes: [
        {
          text: "The only way to do great work is to love what you do.",
          author: "Steve Jobs",
        },
        {
          text: "In three words I can sum up everything I've learned about life: it goes on.",
          author: "Robert Frost",
        },
        {
          text: "Believe you can and you're halfway there.",
          author: "Theodore Roosevelt",
        },
        {
          text: "Success is not final, failure is not fatal: It is the courage to continue that counts.",
          author: "Winston Churchill",
        },
        {
          text: "The only limit to our realization of tomorrow will be our doubts of today.",
          author: "Franklin D. Roosevelt",
        },
        {
          text: "The greatest glory in living lies not in never falling, but in rising every time we fall.",
          author: "Nelson Mandela",
        },
        {
          text: "It is during our darkest moments that we must focus to see the light.",
          author: "Aristotle",
        },
        {
          text: "Life is what happens when you're busy making other plans.",
          author: "John Lennon",
        },
        {
          text: "The purpose of our lives is to be happy.",
          author: "Dalai Lama",
        },
        {
          text: "You have within you right now, everything you need to deal with whatever the world can throw at you.",
          author: "Brian Tracy",
        },
        {
          text: "Don't watch the clock; do what it does. Keep going.",
          author: "Sam Levenson",
        },
        {
          text: "It's not whether you get knocked down, it's whether you get up.",
          author: "Vince Lombardi",
        },
        {
          text: "The best way to predict the future is to create it.",
          author: "Peter Drucker",
        },
        {
          text: "Don't count the days, make the days count.",
          author: "Muhammad Ali",
        },
        {
          text: "Life is 10% what happens to us and 90% how we react to it.",
          author: "Charles R. Swindoll",
        },
      ],
    };

    btn.addEventListener("click", function(){
      let random = Math.floor(Math.random() * quotesData.quotes.length);
      quote.innerText = quotesData.quotes[random].text;
      person.innerText = quotesData.quotes[random].author;
    });
  </script>
</body>
</html>





// language learner app





<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>English Learning Hub</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background-color: #F0F8FF; /* Light blue background */
            color: #333; /* Dark gray text color */
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }

        h1, h2 {
            color: #800000; /* Maroon heading color */
        }

        p {
            font-size: 1.2rem;
        }

        .forum {
            background-color: #FFF; /* White background */
            padding: 20px;
            margin-top: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .button {
            background-color: #800000; /* Maroon button color */
            color: #FFF; /* White text color */
            border: none;
            padding: 10px 20px;
            font-size: 1rem;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        .button:hover {
            background-color: #A52A2A; /* Darker maroon color on hover */
        }

        .thread {
            margin-top: 20px;
            padding: 10px;
            background-color: #F5F5F5; /* Light gray background for threads */
            border-radius: 5px;
        }

        .reply {
            margin-left: 20px;
            padding: 5px;
            background-color: #FAEBD7; /* Antique white background for replies */
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>English Learning Hub</h1>

        <div class="forum">
            <h2>Community Forum</h2>

            <!-- Thread 1 -->
            <div class="thread">
                <h3>How to improve speaking skills?</h3>
                <p>Any tips on improving speaking skills in English?</p>
                <div class="reply">
                    <p>Practice speaking with native speakers regularly.</p>
                </div>
                <div class="reply">
                    <p>Watch English movies and TV shows to improve listening skills.</p>
                </div>
            </div>

            <!-- Thread 2 -->
            <div class="thread">
                <h3>Best online resources for learning English?</h3>
                <p>Share your favorite online resources for learning English.</p>
                <div class="reply">
                    <p>Duolingo and BBC Learning English are great resources.</p>
                </div>
                <div class="reply">
                    <p>I also recommend FluentU and EnglishClub.</p>
                </div>
            </div>

            <!-- Add more threads and replies as needed -->

            <button class="button">Create Thread</button>
        </div>
    </div>
</body>
</html>


fff;
      padding: 20px;
      text-align: center;
    }

    main {
      padding: 20px;
    }

    section {
      margin-bottom: 20px;
    }

    h2 {
      color: #007bff;
    }

    form {
      display: flex;
      flex-direction: column;
      max-width: 300px;
    }

    label {
      margin-bottom: 5px;
    }

    input[type="number"] {
      padding: 5px;
      margin-bottom: 10px;
    }

    button {
      background-color: #007bff;
      color: #fff;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
    }

    button:hover {
      background-color: #0056b3;
    }

    #progress-chart {
      height: 300px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Fitness Tracker</h1>
  </header>
  <main>
    <section id="workout-form">
      <h2>Add Workout</h2>
      <form id="workout-form">
        <label for="exercise-type">Exercise Type:</label>
        <select id="exercise-type">
          <option value="cardio">Cardio</option>
          <option value="strength">Strength Training</option>
          <option value="flexibility">Flexibility</option>
        </select>
        <label for="duration">Duration (minutes):</label>
        <input type="number" id="duration" min="1" required>
        <button type="submit">Add Workout</button>
      </form>
    </section>
    <section id="goals">
      <h2>Set Goals</h2>
      <form id="goals-form">
        <label for="goal">Daily Exercise Goal (minutes):</label>
        <input type="number" id="goal" min="1" required>
        <button type="submit">Set Goal</button>
      </form>
    </section>
    <section id="progress">
      <h2>Progress</h2>
      <div id="progress-chart"></div>
    </section>
  </main>
  <script>
    // Get form elements
    const workoutForm = document.getElementById('workout-form');
    const goalsForm = document.getElementById('goals-form');

    // Add event listeners
    workoutForm.addEventListener('submit', addWorkout);
    goalsForm.addEventListener('submit', setGoal);

    // Function to add workout
    function addWorkout(event) {
      event.preventDefault();
      const exerciseType = document.getElementById('exercise-type').value;
      const duration = parseInt(document.getElementById('duration').value);
      // Add workout to the progress chart
      // This is a placeholder for a real charting library or implementation
      console.log(`Added ${duration} minutes of ${exerciseType} workout.`);
      // You can update the progress chart here
    }

    // Function to set goal
    function setGoal(event) {
      event.preventDefault();
      const goal = parseInt(document.getElementById('goal').value);
      // Store goal in local storage or send it to server
      console.log(`Set daily exercise goal to ${goal} minutes.`);
    }
  </script>
</body>
</html>





// Random quote generator app





<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Quote Generator</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      font-family: Verdana, Geneva, Tahoma, sans-serif;
      box-sizing: border-box;
      line-height: 30px;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      margin: 0 1rem;
      min-height: 100vh;
      text-align: center;
      background: rgb(131, 58, 180);
      background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 41%, rgba(252, 176, 69, 1) 100%);
    }

    .main-content {
      background-color: #e1e1e1;
      padding: 5rem;
      margin-top: 2rem;
      border-radius: 5px;
      text-align: center;
    }

    .container {
      max-width: 768px;
    }

    h1 {
      color: #fff;
    }

    .main-content .quote {
      font-family: 'Times New Roman', Times, serif;
      font-size: 20px;
    }

    .main-content .quote::before {
      content: "“";
      font-size: 20px;
      color: blue;
      font-weight: bold;
      margin-right: 5px;
      opacity: 0.6;
    }

    .main-content .quote::after {
      content: "”";
      font-size: 20px;
      color: blue;
      font-weight: bold;
      margin-left: 5px;
      align-items: center;
    }

    .main-content .person {
      margin-top: 30px;
      font-weight: bold;
      max-width: 100px;
    }

    button {
      padding: 0.75rem 2rem;
      margin-top: 15px;
      background: rgb(131, 58, 180);
      background: linear-gradient(90deg, rgba(131, 58, 180, 1) 0%, rgba(253, 29, 29, 1) 41%, rgba(252, 176, 69, 1) 100%);
      outline: none;
      border: none;
      color: #fff;
      font-weight: bold;
      letter-spacing: 1px;
      border-radius: 4px;
    }

    .quote-container {
      margin-bottom: 15px;
    }
  </style>
</head>
<body>
  <h1>Quote Generator</h1>
  <div class="main-content">
    <div class="quote-container">
      <span class="quote">
        The only way to do great work is to love what you do.
      </span>
    </div>
    <span class="person">
      Steve Jobs
    </span>
  </div>

  <div>
    <button type="button" title="Next Quote" id="nextQuote">Next Quote</button>
  </div>

  <script>
    let quote = document.querySelector(".quote");
    let person = document.querySelector(".person");
    let btn = document.getElementById("nextQuote");

    const quotesData = {
      quotes: [
        {
          text: "The only way to do great work is to love what you do.",
          author: "Steve Jobs",
        },
        {
          text: "In three words I can sum up everything I've learned about life: it goes on.",
          author: "Robert Frost",
        },
        {
          text: "Believe you can and you're halfway there.",
          author: "Theodore Roosevelt",
        },
        {
          text: "Success is not final, failure is not fatal: It is the courage to continue that counts.",
          author: "Winston Churchill",
        },
        {
          text: "The only limit to our realization of tomorrow will be our doubts of today.",
          author: "Franklin D. Roosevelt",
        },
        {
          text: "The greatest glory in living lies not in never falling, but in rising every time we fall.",
          author: "Nelson Mandela",
        },
        {
          text: "It is during our darkest moments that we must focus to see the light.",
          author: "Aristotle",
        },
        {
          text: "Life is what happens when you're busy making other plans.",
          author: "John Lennon",
        },
        {
          text: "The purpose of our lives is to be happy.",
          author: "Dalai Lama",
        },
        {
          text: "You have within you right now, everything you need to deal with whatever the world can throw at you.",
          author: "Brian Tracy",
        },
        {
          text: "Don't watch the clock; do what it does. Keep going.",
          author: "Sam Levenson",
        },
        {
          text: "It's not whether you get knocked down, it's whether you get up.",
          author: "Vince Lombardi",
        },
        {
          text: "The best way to predict the future is to create it.",
          author: "Peter Drucker",
        },
        {
          text: "Don't count the days, make the days count.",
          author: "Muhammad Ali",
        },
        {
          text: "Life is 10% what happens to us and 90% how we react to it.",
          author: "Charles R. Swindoll",
        },
      ],
    };

    btn.addEventListener("click", function(){
      let random = Math.floor(Math.random() * quotesData.quotes.length);
      quote.innerText = quotesData.quotes[random].text;
      person.innerText = quotesData.quotes[random].author;
    });
  </script>
</body>
</html>





// language learner app





<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>English Learning Hub</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background-color: #F0F8FF; /* Light blue background */
            color: #333; /* Dark gray text color */
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }

        h1, h2 {
            color: #800000; /* Maroon heading color */
        }

        p {
            font-size: 1.2rem;
        }

        .forum {
            background-color: #FFF; /* White background */
            padding: 20px;
            margin-top: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .button {
            background-color: #800000; /* Maroon button color */
            color: #FFF; /* White text color */
            border: none;
            padding: 10px 20px;
            font-size: 1rem;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        .button:hover {
            background-color: #A52A2A; /* Darker maroon color on hover */
        }

        .thread {
            margin-top: 20px;
            padding: 10px;
            background-color: #F5F5F5; /* Light gray background for threads */
            border-radius: 5px;
        }

        .reply {
            margin-left: 20px;
            padding: 5px;
            background-color: #FAEBD7; /* Antique white background for replies */
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>English Learning Hub</h1>

        <div class="forum">
            <h2>Community Forum</h2>

            <!-- Thread 1 -->
            <div class="thread">
                <h3>How to improve speaking skills?</h3>
                <p>Any tips on improving speaking skills in English?</p>
                <div class="reply">
                    <p>Practice speaking with native speakers regularly.</p>
                </div>
                <div class="reply">
                    <p>Watch English movies and TV shows to improve listening skills.</p>
                </div>
            </div>

            <!-- Thread 2 -->
            <div class="thread">
                <h3>Best online resources for learning English?</h3>
                <p>Share your favorite online resources for learning English.</p>
                <div class="reply">
                    <p>Duolingo and BBC Learning English are great resources.</p>
                </div>
                <div class="reply">
                    <p>I also recommend FluentU and EnglishClub.</p>
                </div>
            </div>

            <!-- Add more threads and replies as needed -->

            <button class="button">Create Thread</button>
        </div>
    </div>
</body>
</html>



