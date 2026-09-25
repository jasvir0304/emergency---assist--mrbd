<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=600, initial-scale=1.0">

  <title>Emergency Assist MRBD</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      width: 100vw;
      height: 100vh;
      background: #111;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }

    /* 600 × 600 glasses display */
    .display {
      width: 600px;
      height: 600px;
      background: #000;
      color: white;
      position: relative;
      overflow: hidden;
      border: 2px solid #333;
    }

    .screen {
      width: 100%;
      height: 100%;
      padding: 45px;
      display: none;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
    }

    .screen.active {
      display: flex;
    }

    h1 {
      font-size: 42px;
      margin: 10px 0;
    }

    h2 {
      font-size: 30px;
      margin: 15px 0;
    }

    p {
      font-size: 22px;
      line-height: 1.4;
    }

    .emergency-icon {
      font-size: 75px;
      margin-bottom: 20px;
    }

    .menu {
      width: 100%;
      margin-top: 25px;
    }

    .option {
      min-height: 88px;
      width: 100%;
      border: 2px solid #555;
      margin: 12px 0;
      padding: 20px;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 25px;
      border-radius: 12px;
    }

    .option.selected {
      border: 4px solid white;
      background: #222;
    }

    .cancel {
      margin-top: 25px;
      font-size: 20px;
    }

    .countdown {
      font-size: 100px;
      font-weight: bold;
      margin: 20px;
    }

    .status {
      font-size: 26px;
      margin-top: 15px;
    }

    .hint {
      position: absolute;
      bottom: 15px;
      width: 100%;
      text-align: center;
      font-size: 16px;
      color: #aaa;
    }
  </style>
</head>

<body>

  <div class="display">

    <!-- HOME SCREEN -->
    <section id="home" class="screen active">

      <div class="emergency-icon">🚨</div>

      <h1>Emergency Assist</h1>

      <p>
        Emergency assistance is ready.
      </p>

      <div class="menu">

        <div class="option selected" data-action="emergency">
          🚑 Emergency Call
        </div>

        <div class="option" data-action="contact">
          👤 Trusted Contact
        </div>

      </div>

      <div class="hint">
        ↑ ↓ Select &nbsp; | &nbsp; ENTER Confirm
      </div>

    </section>


    <!-- CONFIRMATION SCREEN -->
    <section id="confirm" class="screen">

      <div class="emergency-icon">⚠️</div>

      <h2>Emergency Call?</h2>

      <p>
        Emergency call will start after the countdown.
      </p>

      <div class="menu">

        <div class="option selected" data-action="start">
          YES — START CALL
        </div>

        <div class="option" data-action="cancel">
          NO — CANCEL
        </div>

      </div>

      <div class="hint">
        ↑ ↓ Select &nbsp; | &nbsp; ENTER Confirm
      </div>

    </section>


    <!-- COUNTDOWN SCREEN -->
    <section id="countdownScreen" class="screen">

      <div class="emergency-icon">📞</div>

      <h2>Calling Emergency Service</h2>

      <div id="countdown" class="countdown">
        3
      </div>

      <p>
        Press ESC to cancel.
      </p>

    </section>


    <!-- CALLING SCREEN -->
    <section id="calling" class="screen">

      <div class="emergency-icon">📞</div>

      <h1>Emergency Call</h1>

      <div class="status">
        Call request initiated.
      </div>

      <p>
        Your connected phone should handle the call.
      </p>

      <div class="option selected" id="callButton">
        CALL 112
      </div>

      <div class="option" id="backButton">
        BACK
      </div>

      <div class="hint">
        ENTER to select
      </div>

    </section>


    <!-- TRUSTED CONTACT SCREEN -->
    <section id="contact" class="screen">

      <div class="emergency-icon">👤</div>

      <h2>Trusted Contact</h2>

      <p>
        Contact your saved emergency contact.
      </p>

      <div class="option selected" id="contactButton">
        CONTACT PERSON
      </div>

      <div class="option" id="contactBack">
        BACK
      </div>

      <div class="hint">
        ENTER to select
      </div>

    </section>


    <!-- CANCELLED SCREEN -->
    <section id="cancelled" class="screen">

      <div class="emergency-icon">✓</div>

      <h2>Emergency Cancelled</h2>

      <p>
        No emergency call was started.
      </p>

      <div class="option selected" id="homeButton">
        RETURN HOME
      </div>

      <div class="hint">
        ENTER to continue
      </div>

    </section>

  </div>


<script>

  let currentScreen = "home";
  let selectedIndex = 0;
  let countdownTimer = null;

  const screens = [
    "home",
    "confirm",
    "countdownScreen",
    "calling",
    "contact",
    "cancelled"
  ];

  function showScreen(screenName) {

    screens.forEach(function(screen) {

      document.getElementById(screen)
        .classList.remove("active");

    });

    document.getElementById(screenName)
      .classList.add("active");

    currentScreen = screenName;

    selectedIndex = 0;

    updateSelection();
  }


  function getOptions() {

    const screen = document.getElementById(currentScreen);

    return screen.querySelectorAll(".option");

  }


  function updateSelection() {

    const options = getOptions();

    options.forEach(function(option, index) {

      option.classList.remove("selected");

      if (index === selectedIndex) {
        option.classList.add("selected");
      }

    });

  }


  function moveSelection(direction) {

    const options = getOptions();

    if (options.length === 0) {
      return;
    }

    selectedIndex += direction;

    if (selectedIndex < 0) {
      selectedIndex = options.length - 1;
    }

    if (selectedIndex >= options.length) {
      selectedIndex = 0;
    }

    updateSelection();
  }


  function selectOption() {

    const options = getOptions();

    if (options.length === 0) {
      return;
    }

    const action = options[selectedIndex]
      .getAttribute("data-action");

    if (action === "emergency") {

      showScreen("confirm");

    }

    else if (action === "contact") {

      showScreen("contact");

    }

    else if (action === "start") {

      startCountdown();

    }

    else if (action === "cancel") {

      showScreen("home");

    }

    else {

      handleButton(options[selectedIndex]);

    }
  }


  function handleButton(button) {

    if (button.id === "callButton") {

      /*
        Browser prototype:
        This asks the connected phone/browser
        to handle the emergency number.
      */

      window.location.href = "tel:112";

    }

    else if (button.id === "backButton") {

      showScreen("home");

    }

    else if (button.id === "contactButton") {

      /*
        Replace this with your trusted contact
        number when building the real app.
      */

      alert("Trusted contact feature selected.");

    }

    else if (button.id === "contactBack") {

      showScreen("home");

    }

    else if (button.id === "homeButton") {

      showScreen("home");

    }

  }


  function startCountdown() {

    showScreen("countdownScreen");

    let seconds = 3;

    document.getElementById("countdown")
      .textContent = seconds;

    countdownTimer = setInterval(function() {

      seconds--;

      document.getElementById("countdown")
        .textContent = seconds;

      if (seconds <= 0) {

        clearInterval(countdownTimer);

        showScreen("calling");

      }

    }, 1000);

  }


  function cancelEmergency() {

    if (countdownTimer !== null) {

      clearInterval(countdownTimer);

      countdownTimer = null;

    }

    showScreen("cancelled");

  }


  /*
    Keyboard controls

    Arrow Up    = Previous option
    Arrow Down  = Next option
    Enter       = Select
    Escape      = Cancel
  */

  document.addEventListener("keydown", function(event) {

    if (event.key === "ArrowUp") {

      event.preventDefault();

      moveSelection(-1);

    }

    else if (event.key === "ArrowDown") {

      event.preventDefault();

      moveSelection(1);

    }

    else if (event.key === "Enter") {

      event.preventDefault();

      selectOption();

    }

    else if (event.key === "Escape") {

      event.preventDefault();

      if (currentScreen === "countdownScreen") {

        cancelEmergency();

      }

      else {

        showScreen("home");

      }

    }

  });


  updateSelection();

</script>

</body>
</html>
