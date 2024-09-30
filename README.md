<h1 align="center">
  <a href="https://youtu.be/0U8CVJhdZMk">invisCAPTCHA</a>
</h1>

<p align="center">
  <img src="https://github.com/shoryasethia/invisCAPTCHA/blob/main/invisCAPTCHA.png" alt="invisCAPTCHA">
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=shoryasethia&color=blue&style=flat" alt="Views" />
  <img src="https://img.shields.io/github/stars/shoryasethia/invisCAPTCHA?style=social" alt="GitHub Stars" />
  <img src="https://img.shields.io/github/forks/shoryasethia/invisCAPTCHA?style=social" alt="GitHub Forks" />
</p>

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
### Passive Captcha Defense: Behavioral Analytics and Honeypot Traps with Advanced ML for Bot Detection

### Introduction
Are you tired of proving to every website that you are not a bot or having an identity crisis when it classifies you as a nefarious bot? Are you tired of clicking the never-ending barrage of fire-hydrants? Then we have the perfect solution for you: a State-of-the-Art passive CAPTCHA detection system - **InvisCAPTCHA**.

### Problem Statement
To develop a complete ML-based solution to refine traditional CAPTCHA methods.

Traditional CAPTCHA-based methods rely heavily on user intervention to discriminate the agent as a human or a bot. This is done to protect the limited resources of the server and prevent all the backend APIs from DOS/DDOS-based attacks. In recent times, while the core CAPTCHA technology has remained the same, attacks have become more evolved and sophisticated. Hackers are now exploiting systems protected by CAPTCHA using bots that imitate human behavior or have become smart enough to recognize those optically distorted characters.

While some new solutions exist, like Cloudflare’s Turnstile or Google’s reCAPTCHA, such services are generally expensive for commercial use.

### Objectives
Given the number of users that UIDAI caters to and the per-session costs of third-party CAPTCHA solutions, it is necessary to develop an in-house solution which is both:
1. More secure than traditional CAPTCHA.
2. Requires no/minimal user intervention – Passive implementation.
3. Has minimal overhead of the ML model implemented, to reduce latency and implementation costs.

### Proposed Solution
**InvisCAPTCHA** combines ML methods, statistical techniques like Markov Chains, and "honeypot traps" to efficiently classify user agents. A key differentiator is our use of both parallel and serial models in a multi-level architecture consisting of primary and secondary checks. This greatly improves system efficiency and reduces latency. A detailed summary of our approach is described below:

#### Implementation
**InvisCAPTCHA** uses two different models running in parallel to assign a "user_score" to the agent, segmented into two levels: **Primary** and **Secondary**.

As soon as the score crosses a predetermined threshold (T_H and T_L), the agent is classified as a bot or a human. If classified as a bot, the user is prompted to try again by refreshing the page. If the model cannot determine (the score is between T_H and T_L), the user is redirected to a traditional image-based CAPTCHA for identification.

#### 1. Primary Level
This level consists of **honeypot checks** and a **neural-net based on HTTP methods**. Both pipelines run in parallel and update a global user_score.

- **(a) Honeypot Checks:** These are fake web elements embedded in the UI to fool bots into interacting with them. They are composed of multiple layers:
    - Surface traps like hidden fields and invisible links, visible to bots but invisible to human users.
    - Behavioral traps like fake AJAX calls that simulate dynamic content updates.
    - Logic traps like decoy API endpoints with realistic but non-functional responses. All these checks run simultaneously and classify user agents deterministically.
  
- **(b) HTTP Methods:** This consists of a partially pre-trained neural network that analyzes HTTP requests made by the client and predicts bot probability. The model updates based on real-time requests and internally implements a state-based approach to create a DTMC (Discrete Time Markov Chain).

#### 2. Secondary Level
This level consists of a state-of-the-art LSTM model based on behavioral inputs like mouse movements and keyboard logs during the user's login session. The model is pre-trained on a combination of publicly available datasets and synthetically created data. Other architectures like LightGBM (a Gradient Boosting Decision Tree) were considered for deployment efficiency at the cost of slightly reduced performance.

### Expected Outcomes
During preliminary testing on a limited test dataset, the secondary level model achieved an accuracy exceeding 99%. We plan to conduct further testing on more comprehensive real-world data to refine the model. To counter rapidly evolving bots, we aim to implement “dynamic honeypot traps,” which will learn from bot behavior and update trap placement.

### Conclusion
In a world where bots and adversarial techniques are constantly evolving, we need a system that can evolve in response. **InvisCAPTCHA** uses a multi-layered architecture of different techniques to counter various types of attacks. Its comprehensive pipelined structure makes it adaptable for future needs and easily integrable with the existing UIDAI system.

### Main Problem
Traditional CAPTCHA-based methods rely on user intervention, which burdens users and is less effective against evolving bot technologies. Given the scale and costs associated with using third-party CAPTCHA services, an in-house solution is necessary for UIDAI that is both secure and passive, minimizing user interaction.

A solution combining ML methods with statistical techniques and honeypot traps is proposed. Our key innovation is the use of both parallel and serial models in a multi-level architecture, significantly increasing efficiency while reducing latency.

### Approach
**InvisCAPTCHA** assigns a “user_score” to the agent via two parallel models, with the process divided into Primary and Secondary levels. Based on the score, agents are classified as human or bot, with uncertain cases routed to traditional CAPTCHA for further verification.

- **Primary Level:**
    - Honeypot Checks: Fake elements fool bots.
    - HTTP Methods: Neural network analyzes HTTP requests using a state-based approach.

- **Secondary Level:**
    - Behavioral analysis using LSTM, trained on a mix of real and synthetic data.

### Expected Outcomes:
Preliminary results show over 99% accuracy, with plans to test on broader datasets and implement dynamic honeypot traps for better bot detection in the future.


__________________________________________
> Team info page : [https://shoryasethia.github.io/invisCAPTCHA/](https://shoryasethia.github.io/invisCAPTCHA/)

> Brief Report : [here](https://github.com/shoryasethia/invisCAPTCHA/blob/main/46424-invisCaptcha-SIH-2024.pdf)

> invisCAPTCHA's dummy functionality : [here](https://youtu.be/0U8CVJhdZMk)

```
Updates :
 1. Institutional Round : Cleared Internal Hackathon at IIT Bombay
 2. National Round : in progress
 3. Final Round : --
```
### License
This project is licensed under the MIT License. See the [LICENSE](https://github.com/shoryasethia/invisCAPTCHA/blob/main/LICENSE) file for details.

### Contact
For any inquiries, please contact the [shoryasethia4may@gmail.com](mailto:shoryasethia4may@gmail.com)



