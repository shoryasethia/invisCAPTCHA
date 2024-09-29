# invisCAPTCHA
### Passive Captcha Defense: Behavioural Analytics and Honeypot Traps with Advanced ML Models for Bot Detection
* Tired of proving to every website that that you’re not a bot? We are here to help you out.
* Traditional CAPTCHA methods often require users to solve trivial puzzles or repeatedly identify objects like fire hydrants or traffic
 lights. To tackle this, we introduce a new technique that uses ML and statistical methods to eliminate the need of direct user
 interaction. This involves 2 checks 

  1. Honeypot and HTTP methods act as a Primary Check. HTTP methods employ a two-stage
 classifier. Firstly, a Neural Network estimates the probability of each request being bot generated.
 Then, the Discrete Time Markov Chains classify the user to be bot or human.
  2. Secondary Check exploit Behavioural features (mouse & keyboard logs). These logs are
 continously fed to a LSTM model hosted at the backend. If the final output score obtained, is below
 the threshold, the user is prompted to resort to traditional CAPTCHA method.
 
* All these solutions work in tandem to allow user to do minimal effort to prove that (s)he is not a bot. All these processes run,
 without the user even being aware. The  user is required to engage only when a suspicious behaviour is detected.
* We combine all these methods to come up with a Passive Captcha mechanism. And we also include a HoneyPot test, where we
 lure the bot into a trap which is visible only to a bot. And once a bot falls in that trap, we know for sure it’s a bot.
* We uniquely combine all these methods to eliminate most of the bots, which would have thereby escaped in the case of a single
 test

```
SIH-2024
Team Name: invisCAPTCHA
Team Id: 46424
PS Id: 1672
PS: Develop a ML based solution to refine captcha
Category: Software
Theme: Smart Automation
Ministry: Ministry of Electronics and Information Technology
```
> Project Info Page : [https://shoryasethia.github.io/invisCAPTCHA/](https://shoryasethia.github.io/invisCAPTCHA/)

> Brief Report : [here](https://github.com/shoryasethia/invisCAPTCHA/blob/main/46424-invisCaptcha-SIH-2024.pdf)

```
Updates :
 1. Institutional Round : Cleared Internal Hackathon at IIT Bombay
 2. National Round : in progress
 3. Final Round : --
```
