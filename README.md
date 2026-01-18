# Promptfoo Debugger Challenge

<div align="center">
  <img src="assets/paypal-ai-fail.png" alt="Why we need better AI testing" width="300">
</div>

**This repository is a debugger challenge designed for practicing troubleshooting skills with Promptfoo configuration files.** The `promptfooconfig.yaml` files in this repository intentionally contain errors at different difficulty levels. Your goal is to identify and fix these errors to get the configurations working properly.

The examples use PayPal customer service scenarios to demonstrate why proper AI response testing is crucial - we don't want our AI agents responding "Great!" to users reporting they've been scammed! As you debug these configurations, you'll learn both Promptfoo best practices and develop your troubleshooting skills.

## Project Structure

```
promptfoo-paypal/
├── 1_basic/           # Basic promptfoo setup
├── 2_moderate/        # Intermediate configuration with more features
└── 3_advance/         # Advanced setup with multiple prompts and providers
    ├── prompts/       # Different prompt variations
    ├── providers/     # Provider configurations
    └── tests/         # Test cases and metrics
```

## Video Walkthrough

<div align="center">
  <a href="https://www.youtube.com/watch?v=UYWWO5lDqt8">
    <img src="https://img.youtube.com/vi/UYWWO5lDqt8/0.jpg" alt="Promptfoo PayPal Testing Walkthrough" width="500">
  </a>
  <p>Watch the video walkthrough above to see how this framework helps prevent AI response failures in customer service scenarios.</p>
</div>

## Getting Started

1. Install Promptfoo globally:
   ```bash
   npm install -g promptfoo
   ```

2. Set up your API keys:
   ```bash
   export OPENAI_API_KEY=your_api_key_here
   # Add other provider keys as needed
   ```
   
   Or create the .env file like the .env.example and add your API keys:
    ```bash
    OPENAI_API_KEY="your_key_here"
    ANTHROPIC_API_KEY ="your_key_here"
    # Add other provider keys as needed
   ```

## Challenge Levels

### 1. Basic Setup (1_basic/) - Beginner
- **Challenge:** Fix fundamental YAML syntax errors
- Simple configuration with a single prompt and provider
- Great for getting started and understanding YAML basics
- Once fixed, run with: `cd 1_basic && promptfoo eval`

### 2. Moderate Setup (2_moderate/) - Intermediate
- **Challenge:** Debug indentation and structural errors
- Introduces multiple test cases
- Custom provider settings
- Basic assertion testing
- Once fixed, run with: `cd 2_moderate && promptfoo eval`

### 3. Advanced Setup (3_advance/) - Advanced
- **Challenge:** Identify and correct file path reference errors
- Multiple prompt variations (empathetic vs non-empathetic)
- Different provider configurations (temperature variations)
- Comprehensive test metrics
- Custom test cases and assertions
- Organized file structure
- Once fixed, run with: `cd 3_advance && promptfoo eval`

## How to Use This Debugger Challenge

Each directory contains a `promptfooconfig.yaml` file with intentional errors. To complete the challenge:

1. Navigate to a challenge directory:
   ```bash
   cd 1_basic  # Start with basic, then progress to 2_moderate and 3_advance
   ```

2. Try to run the evaluation and observe the errors:
   ```bash
   promptfoo eval
   ```

3. Debug and fix the errors in `promptfooconfig.yaml`

4. Re-run the evaluation until it succeeds:
   ```bash
   promptfoo eval
   ```

5. View the results to verify everything works:
   ```bash
   promptfoo view
   ```

## Directory Details

### 1_basic/
- Minimal configuration
- Single prompt and provider
- Basic test cases

### 2_moderate/
- Multiple test cases
- Custom provider settings
- Basic assertions
- Output formatting options

### 3_advance/
- `prompts/`: Different prompt variations
  - `empathetic_assistant.txt`: Prompt for empathetic responses
  - `non_empathetic_assistant.txt`: Prompt for direct responses
- `providers/`: Provider configurations
  - `providers_temp_0.7.yaml`: Lower temperature for more focused responses
  - `providers_temp_1.yaml`: Higher temperature for more creative responses
- `tests/`: Test configurations
  - `empathetic_test.yaml`: Tests for empathetic responses
  - `non_empathetic_test.yaml`: Tests for direct responses
  - `test_metrics.yaml`: Custom evaluation metrics

---
Created by Jaime Mantilla, MSIT + AI  
Last Updated: 01/2026 
