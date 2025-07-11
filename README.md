# Weather-India-Survey
<!-- Save this file as "index.html" in your project folder -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>India Weather Survey 2025</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- SEO Meta Tags -->
  <meta name="description" content="Participate in a live weather survey to report conditions across India – May 2025">
  <meta name="keywords" content="India Weather Survey 2025, Heatwave, Rainfall, Climate Change, Weather Feedback">
  <meta name="robots" content="index, follow">

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --primary: #00796b;
      --primary-dark: #004d40;
      --card-bg: #ffffff;
      --text-main: #333;
      --shadow-light: rgba(0, 0, 0, 0.05);
      --shadow-medium: rgba(0, 0, 0, 0.1);
      --radius: 8px;
      --spacing: 1rem;
      --transition: 0.3s;
    }
    *, *::before, *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: 'Roboto', sans-serif;
      background: linear-gradient(135deg, #e0f7fa 0%, #ffffff 100%);
      color: var(--text-main);
      line-height: 1.6;
      padding: var(--spacing);
    }
    header {
      text-align: center;
      margin-bottom: var(--spacing);
    }
    header h1 {
      font-weight: 500;
      font-size: 2rem;
      color: var(--primary-dark);
    }
    header p {
      margin-top: 0.5rem;
      color: var(--primary);
    }
    main {
      max-width: 700px;
      margin: 0 auto;
      background: var(--card-bg);
      border-radius: var(--radius);
      box-shadow: 0 4px 12px var(--shadow-light);
      overflow: hidden;
    }
    form {
      padding: calc(var(--spacing) * 1.5);
      display: flex;
      flex-direction: column;
      gap: var(--spacing);
    }
    label, legend {
      font-weight: 500;
      margin-bottom: 0.25rem;
    }
    input[type="text"],
    input[type="number"],
    select,
    .inline-text {
      width: 100%;
      padding: 0.75rem 1rem;
      border: 1px solid #ccc;
      border-radius: var(--radius);
      transition: border-color var(--transition), box-shadow var(--transition);
      font-size: 1rem;
    }
    input:focus,
    select:focus,
    .inline-text:focus {
      border-color: var(--primary);
      box-shadow: 0 0 0 3px rgba(0, 121, 107, 0.2);
      outline: none;
    }
    fieldset {
      border: none;
      padding: 0;
      margin: 0;
    }
    .checkbox-group {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem 1rem;
      padding: var(--spacing) 0;
    }
    .checkbox-group label {
      display: flex;
      align-items: center;
      gap: 0.25rem;
      font-weight: 400;
    }
    .inline-other {
      display: flex;
      gap: 0.5rem;
      align-items: center;
      margin-top: 0.5rem;
    }
    .inline-text {
      flex: 1;
    }
    button {
      background: var(--primary);
      color: #fff;
      border: none;
      padding: 0.75rem 1.5rem;
      border-radius: var(--radius);
      font-size: 1rem;
      font-weight: 500;
      cursor: pointer;
      align-self: flex-start;
      transition: background var(--transition), box-shadow var(--transition), transform var(--transition);
      box-shadow: 0 2px 6px var(--shadow-light);
    }
    button:hover, button:focus {
      background: var(--primary-dark);
      box-shadow: 0 4px 12px var(--shadow-medium);
      transform: translateY(-2px);
      outline: none;
    }
    footer {
      text-align: center;
      margin-top: var(--spacing);
      font-size: 0.9rem;
      color: #666;
    }
    @media (max-width: 480px) {
      form {
        padding: var(--spacing);
      }
      button {
        width: 100%;
        text-align: center;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>India Weather Survey</h1>
    <p>May 2025 – Real-time Conditions Across India</p>
  </header>

  <main>
    <!-- Replace "your_actual_form_id" with your Formspree form ID -->
    <form action="https://formspree.io/f/your_actual_form_id" method="POST">
      <div>
        <label for="location">1. Your Location (City/State):</label>
        <input
          type="text"
          id="location"
          name="location"
          required
          placeholder="e.g. Mumbai, Maharashtra"
        >
      </div>

      <div>
        <label for="weather">2. Current Weather:</label>
        <select id="weather" name="weather" required>
          <option value="" disabled selected>— Select current weather —</option>
          <option>Very Hot</option>
          <option>Warm</option>
          <option>Pleasant</option>
          <option>Cool</option>
          <option>Cold</option>
          <option>Rainy</option>
          <option>Humid</option>
          <option>Dry</option>
          <option>Stormy/Windy</option>
        </select>
      </div>

      <div>
        <label for="unusual">3. Is this weather unusual for this time of year?</label>
        <select id="unusual" name="unusual" required>
          <option value="" disabled selected>— Select one —</option>
          <option>Yes</option>
          <option>No</option>
          <option>Not Sure</option>
        </select>
      </div>

      <fieldset>
        <legend>4. Weather-related Issues (select all that apply):</legend>
        <div class="checkbox-group">
          <label><input type="checkbox" name="issues" value="Heatwave"> Heatwave</label>
          <label><input type="checkbox" name="issues" value="Heavy Rainfall"> Heavy Rainfall</label>
          <label><input type="checkbox" name="issues" value="Water Shortage"> Water Shortage</label>
          <label><input type="checkbox" name="issues" value="Power Cuts"> Power Cuts</label>
          <label><input type="checkbox" name="issues" value="Poor Air Quality"> Poor Air Quality</label>
          <label><input type="checkbox" name="issues" value="None"> None</label>
        </div>
        <div class="inline-other">
          <label>
            <input type="checkbox" name="issues" value="Other"> Other:
          </label>
          <input
            class="inline-text"
            type="text"
            name="issues_other"
            placeholder="Please specify"
          >
        </div>
      </fieldset>

      <fieldset>
        <legend>5. How are you coping? (select all that apply):</legend>
        <div class="checkbox-group">
          <label><input type="checkbox" name="coping" value="Staying indoors"> Staying indoors</label>
          <label><input type="checkbox" name="coping" value="Using AC/Coolers"> Using AC/Coolers</label>
          <label><input type="checkbox" name="coping" value="Drinking more fluids"> Drinking more fluids</label>
          <label><input type="checkbox" name="coping" value="Wearing light clothes"> Wearing light clothes</label>
          <label><input type="checkbox" name="coping" value="No special measures"> No special measures</label>
        </div>
        <div class="inline-other">
          <label>
            <input type="checkbox" name="coping" value="Other"> Other:
          </label>
          <input
            class="inline-text"
            type="text"
            name="coping_other"
            placeholder="Please specify"
          >
        </div>
      </fieldset>

      <div>
        <label for="comfort">6. Comfort Level (1–5):</label>
        <input
          type="number"
          id="comfort"
          name="comfort"
          min="1"
          max="5"
          required
          placeholder="1 = Very Uncomfortable, 5 = Very Comfortable"
        >
      </div>

      <div>
        <label for="climateChange">7. Do you believe climate change is affecting your region?</label>
        <select id="climateChange" name="climateChange" required>
          <option value="" disabled selected>— Select one —</option>
          <option>Strongly Agree</option>
          <option>Agree</option>
          <option>Neutral</option>
          <option>Disagree</option>
          <option>Strongly Disagree</option>
        </select>
      </div>

      <button type="submit">Submit Survey</button>
    </form>
  </main>

  <footer>
    © 2025 Weather Survey India | Educational Purposes Only
  </footer>

</body>
</html>
