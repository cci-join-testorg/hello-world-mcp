# Prompt Templates

This directory contains structured prompt templates for AI-enabled features. Each prompt template is designed to be testable, reusable, and well-documented.

## Fitness Exercise Recommender (`fitness-exercise-recommender.prompt.yml`)

### Description

A prompt template that provides the top 3 most effective exercises for any given body part. This template is designed for fitness applications where users want targeted exercise recommendations.

### How it Works

- **Input**: Takes a body part name (e.g., "chest", "legs", "back", "shoulders")
- **Output**: Returns exactly 3 exercises with:
  - Exercise name
  - Proper form description
  - Explanation of why it effectively targets the specified muscle group

### Context Schema

```yaml
bodyPart: string # The target body part (e.g., "chest", "legs", "core")
```

### Sample Usage

```yaml
bodyPart: "chest"
```

Expected output: Three chest exercises like push-ups, bench press, and chest flies with detailed form instructions and targeting explanations.

### Tests Included

The template includes 10 comprehensive tests covering:

- Exercise count validation (exactly 3 exercises)
- Completeness of descriptions
- Response formatting and readability
- Appropriate tone and language quality
- Content accuracy and relevance

### Sample Inputs

The template includes sample inputs for common body parts:

- chest
- legs
- back
- shoulders
- arms
- core
- glutes

## File Format

Each prompt template follows this YAML structure:

- `name`: Human-readable name
- `description`: What the template does
- `version`: Semantic version
- `promptOrigin`: Source ("requirements" or "codebase")
- `model`: AI model to use
- `temperature`: Model temperature setting
- `template`: The actual prompt with {{variables}}
- `contextSchema`: Input parameter definitions
- `tests`: Quality validation criteria
- `sampleInputs`: Example input values
