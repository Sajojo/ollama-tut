# Tutorial: Installing Ollama on Your Local Device

Welcome! This guide will help you install Ollama on your local machine. Follow the steps below to get started.

---

## Prerequisites

- A computer running macOS, Linux, or Windows
- Basic familiarity with using the terminal/command prompt

---

## Step 1: Download Ollama

**For macOS:**

Open your terminal and run:
```bash
curl -fsSL https://ollama.com/download/install.sh | sh
```

**For Linux:**

Open your terminal and run:
```bash
curl -fsSL https://ollama.com/download/install.sh | sh
```

**For Windows:**

1. Go to the [Ollama downloads page](https://ollama.com/download).
2. Download the Windows installer.
3. Double-click the installer and follow the prompts.

---

## Step 2: Verify Installation

After installation, check that Ollama is installed by running:

```bash
ollama --version
```

You should see the version number printed. If you get an error, try restarting your terminal or see the troubleshooting section below.

---

#### Step 2.5: Choose a Model

Before running Ollama, you need to choose a model to use. Visit the [Ollama Models page](https://ollama.com/library) to browse available models.  
Pick a model you prefer—some popular options include `llama2`, `mistral`, or `phi3`.  
Take note of the model name, as you’ll use it in the next step.

---

## Step 3: Run Ollama

Start Ollama by running (replace `llama2` with your chosen model):

```bash
ollama run llama2
```

For example, to run the `mistral` model:

```bash
ollama run mistral
```

---

## Troubleshooting

- **Command not found:** Make sure you closed and reopened your terminal after installing.
- **Permissions error:** Try running the install command with `sudo` (Linux/macOS).
- If you continue having issues, visit the [Ollama documentation](https://ollama.com/docs) or open an issue in this repository.

---

## Additional Resources

- [Ollama Official Website](https://ollama.com/)
- [Ollama Documentation](https://ollama.com/docs)
- [Ollama Models Library](https://ollama.com/library)
- [Community Forum](https://ollama.com/community)

---