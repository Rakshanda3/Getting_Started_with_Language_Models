# Getting_Started_with_Language_Models

## Prerequisites
Before you begin, ensure you have the following:

1. **Git**: [Install Git](https://git-scm.com/) from its official website.  
2. **Docker**: [Install Docker](https://www.docker.com) from its official website.  
3. **Groq API Key**: [Log in to the Groq Console](https://console.groq.com) to generate a new API key.  
4. **Linux/MacOS**: No extra setup needed.  
5. **Windows**: Install [WSL](https://learn.microsoft.com/en-us/windows/wsl/install) and enable Docker's WSL integration by following [this guide](https://docs.docker.com/desktop/windows/wsl/).  

---

### Step 1: Clone the Repository
Clone the GitHub repository to your local machine:  
```bash
git clone https://github.com/Rakshanda3/Getting_Started_with_Language_Models.git
```

### Step 2: Navigate to the Repository
Change to the cloned repository directory:  
```bash
cd Getting_Started_with_Language_Models
```

### Step 3: Pull the Latest Version
Update the repository to the latest version:  
```bash
git pull origin main
```

### Step 4: Modify Script Permissions
Enable execute permissions for the setup script:  
```bash
chmod u+x docker_image_setup.sh
```

### Step 5: Build and Run the Docker Container
> **⚠️ Warning**: Ensure port `8888` is free. The script will automatically clean up this port if it's in use by stopping and removing any Docker container using it.

Run the setup script to build and start the Docker container:  
```bash
docker build -t getting_started_with_language_models .
```

### Step 6: Run the Docker Container
Run the Docker container and map the ports. This will allow you to access Jupyter Notebook at port 8888:
```bash
docker run -p 8888:8888 -v $(pwd):/usr/src/app getting_started_with_language_models
```

### Step 7: Access the Jupyter Notebook
- Once the container starts, the terminal will display a URL (e.g., `http://127.0.0.1`) with a token.  
- Copy and paste this URL into your browser to access the Jupyter Notebook interface.   
