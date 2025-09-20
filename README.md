📡Electronic Voting Machine using Arduino Uno

An Arduino Uno-based Electronic Voting Machine (EVM) designed to provide a secure, cost-effective, and efficient voting solution. The system uses push buttons for candidate selection, an LCD display for live vote count, and LED indicators for visual feedback. This project demonstrates the potential of microcontroller-based systems in modernizing elections.


---
🔎 Introduction

Electronic Voting Machines (EVMs) simplify the voting process by eliminating paper ballots and manual counting errors. This project implements a mini EVM prototype using Arduino Uno. The design ensures transparency, fast results, and ease of use, making it suitable for small-scale elections in schools, colleges, and communities.


---
⚡ Circuit Diagram


<img width="1280" height="723" alt="image" src="https://github.com/user-attachments/assets/1fc04daf-be6f-43e3-9cbf-24b57df0c36f" />



Button → Arduino Pin (D2-D5)  
LEDs   → Arduino Pin (D12-D13)  
LCD    → Arduino Pin (6-11)  
Power  → 5V + GND from Arduino


---


⚙ How It Works

1. Power on the device. LCD displays candidate names.


2. Voter presses a button to cast a vote.


3. Green LED lights up briefly to confirm vote.


4. Votes are counted and stored in Arduino memory.


5. When the result button is pressed:

Red LED lights up.

LCD displays the winning candidate or "Tie/No Result".



6. After result display, votes reset automatically for the next session.




---
⚙ Working

The Arduino-based Electronic Voting Machine (EVM) operates in a series of simple but secure steps:

🔹 1. Initialization

When powered on, the Arduino initializes the LCD display, LEDs, and button inputs.

The LCD displays the title "Voting Machine" and then lists the available candidates (e.g., A, B, C, D).

All vote counters are reset to zero, ensuring a fresh start for every new session.




🔹 2. Voting Process

Each candidate is assigned a push button.

A voter presses the button corresponding to their chosen candidate.

The Arduino detects the button press using digitalRead() and increments the respective candidate’s vote counter.

A green LED blinks briefly to confirm that the vote has been registered.

The vote count is updated instantly and displayed on the LCD.




🔹 3. Debouncing & Single-Vote Handling

To prevent multiple votes from a single press, the code includes debouncing logic.

The Arduino waits until the button is fully released before allowing another input.

This ensures that each voter can only cast one vote per session.



🔹 4. Result Declaration

Once all voters have cast their votes, the result button is pressed by an authorized person.

The Arduino adds up the total votes and compares candidate counters.

A red LED lights up to indicate the result phase.

The LCD then displays the winner:

Example: “Candidate A Wins”

If two or more candidates have the same highest vote count, the LCD shows “Tie Up or No Result”.

If no votes are cast, the LCD displays “No Voting”.





🔹 5. Reset Mechanism

After showing results for a few seconds, the system:

Resets all vote counters back to zero.

Clears the LCD display.

Turns off all LEDs.


This prepares the machine for the next voting session.



🔹 6. Security & Reliability

Each button press is confirmed with both visual (LED blink) and text feedback on the LCD.

The system ensures tamper resistance by allowing only one vote per button press.

Vote counts are stored temporarily in Arduino memory and cleared only after the result declaration.



---
💯Result

before
<img width="772" height="837" alt="image" src="https://github.com/user-attachments/assets/819f0935-cc60-4f2a-9af8-aeae8b2b25d7" />

After
<img width="690" height="840" alt="image" src="https://github.com/user-attachments/assets/33883187-2fa8-4d1a-8fc1-34e48cdcd0de" />



📌 Applications

School and college elections

Small community or organizational polls

Corporate board voting

Prototyping for advanced voting systems



---

✅ Advantages

Cost-effective and portable

Easy to use with simple interface

Faster result processing

Reduces human error in counting

Eco-friendly (no paper ballots)

Modular design for expansion



---

⚠ Limitations

Suitable only for small-scale elections

Limited security features (basic authentication)

Dependent on continuous power supply

Button or display failure may affect reliability

Lacks biometric or RFID-based voter authentication



---
✨ Features

Arduino Uno as the control unit

Push buttons for candidate selection

16x2 LCD display for live vote count & results

LED indicators for successful vote casting

Reset functionality for new voting sessions

User-friendly and cost-effective design




🚀 Future Enhancements

Integration with RFID or fingerprint modules for voter authentication

Adding EEPROM/SD card for permanent vote storage

Wireless connectivity for remote monitoring

Enhanced security features (encryption, tamper-proof casing)

Support for larger number of candidates



---
✅ This working model ensures a fair, accurate, and transparent voting process, making it a reliable prototype for small-scale elections.
