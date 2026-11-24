[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/erodriguezlois/D4S-Grand-Challenge/blob/main/GrandChallenge.ipynb) 
[![Open Google Form](https://img.shields.io/badge/Submit%20via-Google%20Form-4285F4?style=flat&logo=googleforms&logoColor=white)](https://forms.gle/jbxpevwEbKDUyxGs6)

# 🛡️ D4S: Robust DCT-Watermarking Grand Challenge

Welcome to the **D4S: Robust DCT-Watermarking Grand Challenge**! Your goal is to build a blind, DCT-domain image watermarking system (`watermark_encoder` and `watermark_decoder`) using PNG file I/O that achieves **Zero Errors (BER = 0)** under JPEG compression attacks while minimizing perceptual distortion (**Mean LPIPS**).

> **🔑 Account Requirement:** You will need a **Google account** to run the notebook in **Google Colab** and upload your submission through the **Google Form**.

> **⏰ Submission Deadline:** **Friday, 15th of January 2027 at 14:00 UTC+1**.

### 1. Access the Notebook & Run It
1. **Open the GitHub Repository:** Go to the challenge's GitHub repository and locate the public starter/evaluation notebook ([GrandChallenge.ipynb](https://colab.research.google.com/github/erodriguezlois/D4S-Grand-Challenge/blob/main/GrandChallenge.ipynb)).
2. **Launch in Google Colab & Save a Copy (Recommended):** Sign in with your Google account and open the notebook in **Google Colab** (you can also run it locally, though testing in Colab is strongly advised so your environment, dependencies, and paths match the automated grading setup). Because the repository notebook opens in view/read-only mode, select **File → Save a copy in Drive** to edit your code and save your changes.
3. **Run Local Self-Evaluation:** Execute the setup and **Local Self-Evaluation** cells against `public_test/` to verify your `watermark_encoder` and `watermark_decoder` implementation, inspect the binary-searched `strength` values (0–250), and aim for **No decoding errors (BER = 0)** with low **Mean LPIPS**.

### 2. Submit Your Solution
1. **Name Your File Properly:** Save your standalone code as `<pseudonym>.py` using **only lowercase letters, digits, and underscores** (for example, `blue_fox.py`), including `PSEUDONYM = "<pseudonym>"`, `watermark_encoder(...)`, and `watermark_decoder(...)`.
2. **Upload via the Google Form:** Sign in with your Google account and submit your `.py` file through the official Google Form ([https://forms.gle/jbxpevwEbKDUyxGs6](https://forms.gle/jbxpevwEbKDUyxGs6)) before **Friday, 15th of January 2027 at 14:00 UTC+1**.
3. **Check the Leaderboard:** Grading runs **once daily** (timestamps displayed in **UTC+1**). Re-run `view_leaderboard()` after the next update to check your rank, or call `see_all_submissions("<pseudonym>")` to inspect your history. Keep in mind that **at most 2 ungraded submissions per participant** are evaluated per run (keeping the first two), and top leaderboard scores still undergo manual review for genuine DCT-domain embedding and rule compliance.

### 📊 Grading Scale
Final grades are determined by **Mean LPIPS** (assuming **No decoding errors (BER = 0)** and compliance with challenge rules):

| Mean LPIPS Threshold | Grade |
| :--- | :--- |
| Less than `5e-3` | **A (Sobresaliente)** |
| Less than `0.2` | **B (Notable)** |
| Less than `0.26` | **C (Aprobado)** |
| Greater than or equal to `0.26` | **F (Suspenso)** |
