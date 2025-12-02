# 🚀 GitHub Repository Access Audit Script  

A Bash-based automation tool that lists all collaborators of a GitHub repository and identifies users with read permissions — executed from an AWS EC2 Ubuntu server using the GitHub REST API.

---

## 📌 Overview  
This script automates the process of checking who has access to a GitHub repository.  
By supplying your GitHub username, API token, organization/user name, and repository name, the script connects to the GitHub REST API and returns:

- ✔️ All collaborators  
- ✔️ Users with **read (pull)** permissions  
- ✔️ Clean, formatted output  
- ✔️ Faster audit compared to manual GitHub UI checking  

This is especially useful for DevOps teams who need visibility over repository access and permission levels.

---

## 🛠️ Technologies Used  
- **Bash**  
- **GitHub REST API**  
- **curl**  
- **jq**  
- **AWS EC2 (Ubuntu t2.micro)**  

---

## 📂 Script Features  
- Authenticates with GitHub API using username + Personal Access Token  
- Retrieves all collaborators of a chosen repository  
- Filters and prints users with **read (pull)** access  
- Secure token handling using **environment variables**  
- Works smoothly on EC2 Linux servers  

---

## ⚙️ Setup Instructions  

### 1️⃣ Clone This Repository  
```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

### 2️⃣ Install Dependencies  
```bash
sudo apt update
sudo apt install -y jq curl git
```

### 3️⃣ Set Your GitHub Credentials as Environment Variables  
```bash
export username="your_github_username"
export token="your_github_pat"
```

> **Note:** Never hard-code or commit your token into the script.

---

## ▶️ Run the Script  

### Syntax  
```bash
./list_collabs.sh <repo-owner-or-org> <repository-name>
```

### Example  
```bash
./list_collabs.sh my-organization sample-repo
```

### Sample Output  
```
Listing users with read access to my-organization/sample-repo...
Users with read access:
dev-user-1
team-member-2
qa-engineer-3
```

---

## 🔐 Security Notes  
- Always use environment variables for storing sensitive tokens  
- Never commit real tokens to GitHub  
- Regenerate/revoke tokens if exposed accidentally  

---

## 🎯 What I Learned  
- GitHub API integration using Bash  
- JSON parsing with jq  
- Secure token usage with environment variables  
- Running DevOps scripts on AWS EC2  
- Automating repository access audits  

---

## 📈 Future Enhancements  
- Add detection for write/admin permissions  
- Export results to CSV or JSON  
- Automate daily audits with cron jobs  
- Add Slack or email alerts  
- Implement GitHub Actions automation  

---

## 🤝 Contributions  
Contributions and suggestions are welcome!  
Feel free to open issues or submit pull requests.

