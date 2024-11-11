# Llama-impact Codegen
- Set up and configure the Py API.
- Learn to interact with different endpoints to manage dependencies.
- Understand the process of automating dependency updates in a GitHub repository.

---

🔧 Motivation: 
- Regular infrastructure upgrades are essential for performance, security, and sustainability. 
- Building long-term solutions, not just short-term fixes, helps ensure smooth, efficient operations.

⚠️ The Problem:
- Managing dependencies becomes complex as codebases grow.
- It's time-consuming, costly, and increases the risk of failures.
- Scaling services and maintaining fast development cycles are major challenges.

💡 How Big is the Problem?
- Downtime can cost Fortune 1,000 companies up to $1 million per hour (IDC survey). 
- Large enterprises might spend $60 million or more on incidents annually (IHS Research).

✅ Our Solution: Progressive automation, moving from manual support to full automation maturity. 

---

## Instructions

### Step 1: Clone the Workshop Repository
If you haven't cloned the repository already, run:
```bash
git clone https://github.com/sakomw/ai-workshop.git
cd ai-workshop/sessions/session_1
```

### Step 2: Set Up Environment
- Setup secrets in backend/.env.local and name it .env:
```
GITHUB_TOKEN=x
GROQ_API_KEY=x
```
- Install [flox](https://flox.dev):
  ```bash
  brew install flox
  flox activate
  ```
- Install any necessary dependencies for backend:
  ```bash
  cd backend
  pip install -r requirements.txt
  uvicorn main:app --reload
  ```

- See the directory structure in backend:
```
├── cf_aiproxy.py
├── config.py
├── main.py
├── models
│   ├── __init__.py
│   └── schemas.py
├── requirements.txt
├── routes
│   ├── __init__.py
│   └── api_routes.py
└── services
    ├── __init__.py
    ├── dependency_service.py
    └── github_service.py
```

- Install any necessary dependencies for the frontend:
  ```bash
  cd frontend
  yarn install
  yarn dev
  ```

### Step 3: Demo
- Open in browser and select the repo with requirements.txt file in root folder: http://localhost:3000

[demo](https://www.loom.com/share/945f48e6182c496582da85854e313a9b?sid=f5673e5d-262b-4048-bbee-22abe53d03b6)
