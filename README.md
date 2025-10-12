# Promptfoo Examples with PayPal Fail Scenario

<div align="center">
  <img src="assets/paypal-ai-fail.png" alt="Why we need better AI testing" width="300">
</div>

This repository contains examples of different approaches to setting up and using Promptfoo for testing and evaluating AI prompts, with a focus on PayPal-related scenarios. The examples are organized in three levels of complexity: basic, moderate, and advanced. The example above shows why proper AI response testing is crucial - we don't want our AI agents responding "Great!" to users reporting they've been scammed!

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

## Example Levels

### 1. Basic Setup (1_basic/)
- Simple configuration with a single prompt and provider
- Great for getting started and understanding the basics
- Uses default settings for most options
- Run with: `cd 1_basic && promptfoo eval`

### 2. Moderate Setup (2_moderate/)
- Introduces multiple test cases
- Custom provider settings
- Basic assertion testing
- Run with: `cd 2_moderate && promptfoo eval`

### 3. Advanced Setup (3_advance/)
- Multiple prompt variations (empathetic vs non-empathetic)
- Different provider configurations (temperature variations)
- Comprehensive test metrics
- Custom test cases and assertions
- Organized file structure
- Run with: `cd 3_advance && promptfoo eval`

## Running Tests

Each directory contains its own `promptfooconfig.yaml` file. To run tests:

1. Navigate to the desired example directory:
   ```bash
   cd 1_basic  # or 2_moderate or 3_advance
   ```

2. Run the evaluation:
   ```bash
   promptfoo eval
   ```

3. View the results:
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
Last Updated: 08/2025 
