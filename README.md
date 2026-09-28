# 🔐 SQROCK IT Solution — Cybersecurity Internship

# Day 9: Social Media Impersonation & Fake Profile Detection

![Kali Linux](https://img.shields.io/badge/Kali_Linux-2026.2-557C94?logo=kalilinux\&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.13.12-3776AB?logo=python\&logoColor=white)
![Social Engineering](https://img.shields.io/badge/Social_Engineering-Awareness-blue)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Training-red)
![OSINT](https://img.shields.io/badge/OSINT-Analysis-orange)
![Fake Profile Detection](https://img.shields.io/badge/Fake_Profile-Detection-purple)
![Threat Awareness](https://img.shields.io/badge/Threat-Awareness-yellow)
![Defensive Security](https://img.shields.io/badge/Defensive-Security-green)
![Ethical Hacking](https://img.shields.io/badge/Ethical-Hacking-blue)
![Lab Only](https://img.shields.io/badge/Environment-Local_Lab-lightgrey)

---

## 📌 Project Overview

As part of **Day 9 of the SQROCK IT Solution Cybersecurity Internship**, this project focuses on **social media impersonation, fake profiles, and online identity deception**.

Social media platforms can be abused by individuals who create fraudulent profiles to impersonate legitimate users, deceive victims, collect information, or establish trust before conducting social engineering attacks.

The purpose of this project was to develop a **Python-based fake-profile scoring tool** that evaluates selected profile characteristics and assigns an awareness-oriented risk score.

The assessment uses **anonymized and fictional sample profiles** rather than real individuals.

The tool evaluates characteristics such as:

* Account age
* Follower/following ratio
* Profile-picture availability
* Number of posts
* Biography information

The project demonstrates how multiple indicators can be combined to support **security awareness and preliminary risk assessment**.

> **Important:** The scoring system is an educational heuristic. A high score does not prove that an account is fake, malicious, or operated by an attacker.

---

## 🎯 Objectives

The main objectives of this project were to:

* Understand social media impersonation techniques.
* Understand how fake profiles can support social engineering.
* Identify common indicators associated with suspicious profiles.
* Develop a Python-based profile-scoring tool.
* Evaluate five anonymized sample profiles.
* Analyze account age and engagement characteristics.
* Examine follower/following ratios.
* Identify missing profile information.
* Generate an awareness-oriented risk assessment.
* Develop defensive recommendations for social media users.
* Practice ethical OSINT and cybersecurity analysis.

---

## 🛠️ Tools and Technologies Used

| Tool / Technology       | Purpose                                   |
| ----------------------- | ----------------------------------------- |
| **Kali Linux 2026.2**   | Cybersecurity laboratory environment      |
| **Python 3.13.12**      | Fake-profile scoring tool                 |
| **Python Dictionaries** | Representing profile information          |
| **Python Functions**    | Automating profile analysis               |
| **Terminal**            | Running the Python program                |
| **Nano**                | Creating and editing files                |
| **Markdown**            | Analysis and documentation                |
| **Git & GitHub**        | Version control and project documentation |

---

## 🧠 Skills Demonstrated

* Social media security analysis
* Fake-profile detection
* Social engineering awareness
* OSINT concepts
* Python programming
* Data analysis
* Risk scoring
* Threat identification
* Defensive cybersecurity
* Critical analysis
* Security documentation
* Ethical security research

---

## 🔬 Understanding Social Media Impersonation

Social media impersonation occurs when someone creates or uses an online identity that falsely represents another person, organization, or entity.

A simplified social engineering process can be represented as:

```text
┌──────────────────────────┐
│ Information Gathering    │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│ Fake / Impersonated      │
│ Social Media Profile     │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│ Establish Trust          │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│ Social Engineering       │
│ Attempt                  │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│ Potential Victim Impact  │
└──────────────────────────┘
```

The goal of this project was to understand the **warning signs** that may help users recognize suspicious profiles before interacting with them.

---

## 🎯 Profile Indicators Used

The scoring tool evaluates five main characteristics.

### 1. Account Age

Very recently created accounts may require additional scrutiny, particularly when combined with other suspicious characteristics.

### 2. Follower/Following Ratio

An unusual ratio between followers and accounts followed can sometimes provide useful context.

However, this indicator alone does not prove that a profile is fraudulent.

### 3. Profile Picture

A missing or generic profile picture can be a warning sign, although legitimate users may also choose not to use a profile photograph.

### 4. Number of Posts

An account with very little activity may warrant additional review when other indicators are also present.

### 5. Biography

An empty, generic, or inconsistent biography can provide another contextual indicator.

---

## 🔬 Methodology

The project was completed using the following methodology.

### Step 1 — Define Detection Indicators

Five profile characteristics were selected:

```text
Account Age
Follower/Following Ratio
Profile Picture
Number of Posts
Biography
```

---

### Step 2 — Create Anonymized Sample Profiles

Five fictional profiles were created for testing.

Example structure:

```python
profile = {
    "username": "sample_user",
    "account_age_days": 30,
    "followers": 12,
    "following": 850,
    "has_profile_picture": False,
    "posts": 1,
    "has_bio": False
}
```

The profiles do not represent real individuals.

---

### Step 3 — Define a Scoring System

Each suspicious characteristic contributes points to an awareness score.

For example:

| Indicator               | Example Condition                         | Score |
| ----------------------- | ----------------------------------------- | ----: |
| Very new account        | Account below defined age threshold       |    +2 |
| Unusual ratio           | Very high following relative to followers |    +2 |
| Missing profile picture | No profile picture                        |    +1 |
| Very few posts          | Minimal account activity                  |    +1 |
| Missing biography       | No biography information                  |    +1 |

The final score is calculated from the combined indicators.

---

## 💻 Python Implementation

The project was implemented using Python.

A simplified scoring function follows this structure:

```python
def score_profile(profile):
    score = 0
    indicators = []

    if profile["account_age_days"] < 90:
        score += 2
        indicators.append("Very new account")

    if profile["following"] > profile["followers"] * 10:
        score += 2
        indicators.append("Unusual follower/following ratio")

    if not profile["has_profile_picture"]:
        score += 1
        indicators.append("Missing profile picture")

    if profile["posts"] < 5:
        score += 1
        indicators.append("Very few posts")

    if not profile["has_bio"]:
        score += 1
        indicators.append("Missing biography")

    return score, indicators
```

The scoring logic is intended for **educational awareness**, not automated accusations or definitive identity verification.

---

## 📊 Risk Interpretation

An example educational interpretation can be:

| Score | Awareness Level | Interpretation                                  |
| ----: | --------------- | ----------------------------------------------- |
|   0–1 | Low             | Few selected indicators detected                |
|   2–3 | Moderate        | Some indicators require additional review       |
|   4–5 | Elevated        | Multiple indicators detected                    |
|    6+ | High            | Several indicators warrant careful verification |

> These categories are heuristic labels for the training exercise. They should not be treated as proof that an account is fraudulent.

---

## 🧪 Five Sample Profiles

The tool was tested against five anonymized profiles.

Example test dataset:

```text
Profile A → Established account with normal activity
Profile B → Recently created account
Profile C → Missing profile picture and biography
Profile D → Unusual follower/following ratio
Profile E → Multiple suspicious indicators
```

The profiles were intentionally designed to represent different combinations of characteristics.

---

## 📈 Analysis Process

For each profile, the Python tool:

```text
Profile Data
     │
     ▼
Indicator Evaluation
     │
     ├── Account Age
     ├── Follower/Following Ratio
     ├── Profile Picture
     ├── Post Activity
     └── Biography
     │
     ▼
Risk Score Calculation
     │
     ▼
Detected Indicators
     │
     ▼
Awareness Assessment
```

This approach demonstrates how simple rule-based analysis can assist with security awareness.

---

## 📂 Project Structure

```text
day9-fake-profile-detection/
│
├── fake_profile_detector.py
├── sample_profiles.json
├── profile_analysis.txt
├── analysis.md
└── README.md
```

### File Description

| File                       | Description                        |
| -------------------------- | ---------------------------------- |
| `fake_profile_detector.py` | Python profile-scoring tool        |
| `sample_profiles.json`     | Five anonymized fictional profiles |
| `profile_analysis.txt`     | Generated analysis results         |
| `analysis.md`              | Detailed security analysis         |
| `README.md`                | Project documentation              |

---

## ⚙️ Environment Configuration

The project directory was created using:

```bash
mkdir -p ~/sqrock-internship/day9-fake-profile-detection
cd ~/sqrock-internship/day9-fake-profile-detection
```

Python was verified with:

```bash
python3 --version
```

Expected environment:

```text
Python 3.13.12
```

The Python script can be created using:

```bash
nano fake_profile_detector.py
```

The program can then be executed with:

```bash
python3 fake_profile_detector.py
```

To save the results:

```bash
python3 fake_profile_detector.py > profile_analysis.txt
```

The results can be viewed using:

```bash
cat profile_analysis.txt
```

---

## 🧪 Laboratory Environment

The project was conducted in an authorized cybersecurity training environment.

```text
Operating System : Kali Linux 2026.2
Python           : 3.13.12
Environment      : Local Cybersecurity Lab
Data Type        : Fictional / Anonymized
External Targets : None
Real Profiles    : None
```

### Laboratory Architecture

```text
┌─────────────────────────────────────┐
│          Kali Linux 2026.2         │
│                                     │
│   ┌─────────────────────────────┐   │
│   │  Fictional Profile Dataset  │   │
│   └──────────────┬──────────────┘   │
│                  │                  │
│                  ▼                  │
│   ┌─────────────────────────────┐   │
│   │ Python Fake Profile         │   │
│   │ Detection Tool              │   │
│   └──────────────┬──────────────┘   │
│                  │                  │
│                  ▼                  │
│   ┌─────────────────────────────┐   │
│   │ Indicator Analysis &        │   │
│   │ Risk Scoring                │   │
│   └──────────────┬──────────────┘   │
│                  │                  │
│                  ▼                  │
│   ┌─────────────────────────────┐   │
│   │ Security Awareness Report   │   │
│   └─────────────────────────────┘   │
└─────────────────────────────────────┘
```

---

## 🔎 Common Fake-Profile Warning Signs

Users should consider additional verification when several of the following appear together:

* Recently created account.
* Very little account activity.
* Missing or generic profile picture.
* Incomplete biography.
* Unusual follower/following ratio.
* Inconsistent profile information.
* Repeated generic posts.
* Unexpected friend or follow requests.
* Pressure to move conversations to another platform.
* Requests for sensitive information.
* Suspicious links.
* Requests involving money, credentials, or verification codes.

A single indicator should **not** automatically be treated as evidence of a fake account.

---

## 🛡️ Defensive Measures

### 1. Verify Identity

Use independent and trusted channels to confirm someone's identity when necessary.

### 2. Avoid Sharing Sensitive Information

Do not provide passwords, MFA codes, financial information, or other sensitive data through unsolicited social media interactions.

### 3. Inspect Account History

Look at the account's age, activity, posts, and interactions.

### 4. Check for Inconsistencies

Compare names, profile information, photographs, and other publicly available details for inconsistencies.

### 5. Be Careful With Links

Avoid clicking suspicious links received from unknown accounts.

### 6. Use Platform Reporting Features

Suspicious impersonation accounts should be reported through the relevant platform's official reporting mechanisms.

### 7. Enable MFA

Multi-factor authentication provides additional protection if account credentials become compromised.

### 8. Limit Public Information

Avoid unnecessarily exposing personal information that could be used for social engineering.

---

## 📊 Results

The project successfully demonstrated how a Python-based rule system can analyze fictional social media profiles and identify predefined warning indicators.

The exercise showed that:

* Multiple indicators can be combined into an awareness score.
* Recently created accounts may require additional scrutiny.
* Unusual follower/following patterns can provide contextual information.
* Missing profile information can contribute to a suspicious-profile assessment.
* Automated scoring should support human review rather than replace it.
* No individual indicator is sufficient to conclusively identify a fake profile.

---

## ⚠️ Limitations of the Detection Tool

The scoring tool has important limitations.

### Rule-Based Detection

The tool relies on predefined rules and thresholds.

### False Positives

A legitimate account may exhibit characteristics that appear suspicious.

For example, a new user may legitimately have:

* Few followers.
* Few posts.
* No profile picture.
* An incomplete biography.

### False Negatives

A sophisticated fraudulent profile may contain realistic information and therefore avoid several simple detection indicators.

### No Identity Verification

The tool does not verify the actual identity of an account owner.

Therefore:

> **The score represents an educational risk indicator, not a determination that an account is fake.**

---

## 🔐 Security and Ethical Considerations

This project was conducted strictly for **authorized cybersecurity education and awareness training**.

The following safeguards were maintained:

* Only fictional/anonymized profiles were used.
* No real individuals were targeted.
* No accounts were accessed.
* No credentials were collected.
* No social media accounts were impersonated.
* No automated interaction with social media platforms was performed.
* No unauthorized OSINT collection was conducted.
* The project remained within the controlled laboratory environment.

---

## 🎓 Learning Outcomes

After completing this project, I gained practical understanding of:

* Social media impersonation.
* Fake-profile characteristics.
* Social engineering risks.
* OSINT concepts.
* Rule-based risk scoring.
* Python dictionaries and functions.
* Data-driven security analysis.
* Defensive social media practices.
* False positives and false negatives.
* Ethical cybersecurity research.
* Security awareness and threat identification.

---

## 📚 Key Security Concepts

```text
              Social Media Profile
                       │
                       ▼
              Profile Indicators
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
   Account Age    Profile Data    Activity
        │              │              │
        └──────────────┼──────────────┘
                       ▼
                Rule-Based Analysis
                       │
                       ▼
                  Risk Score
                       │
                       ▼
               Human Verification
                       │
          ┌────────────┴────────────┐
          ▼                         ▼
       Suspicious                Legitimate
       Indicators                Possibility
```

---

## 🏆 Project Conclusion

Day 9 provided practical experience in **social media security, fake-profile detection, OSINT concepts, social engineering awareness, and Python-based risk analysis**.

By creating a rule-based profile-scoring tool and testing it against five fictional profiles, the project demonstrated how publicly visible profile characteristics can be organized into an educational security assessment.

The project also highlighted an important cybersecurity principle: **automated indicators should support human analysis rather than be treated as definitive proof of malicious activity**.

This exercise strengthened my skills in **Python programming, cybersecurity analysis, social engineering awareness, OSINT concepts, risk assessment, and ethical security practices**.

---

# 👤 Author

Atemlefac Nkafu Bechem

Cybersecurity Engineer

LinkedIn: https://www.linkedin.com/in/atemlefac-nkafu-bechem-179987248

📌 Project Information Program Name: Cybersecurity internship at SQROCK | Week: 02 | Project 9: Social Media Impersonation & Fake Profile Detection | Repository: GitHubing
