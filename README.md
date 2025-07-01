# xml-prompt

A lightweight library enabling React (and MDX) developers to write large language model (LLM) prompts as JSX components. xml-prompt brings the power of component-based architecture to prompt engineering.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![React](https://img.shields.io/badge/React->=16.8.0-61DAFB)
![Node](https://img.shields.io/badge/Node->=14.0.0-339933)
![License](https://img.shields.io/badge/license-MIT-green)
![Last Updated](https://img.shields.io/badge/last%20updated-2025--07--01-yellowgreen)

## Features

- 🎯 Write prompts using familiar JSX syntax
- 📝 Author prompts in MDX for enhanced documentation
- 🧩 Build complex prompts from reusable components
- 🔍 Type safety with TypeScript support
- 🎨 Clear separation of concerns
- 📦 Component-based prompt composition
- 🔄 Improved prompt maintenance

## Installation

```bash
# npm
npm install xml-prompt

# yarn
yarn add xml-prompt
```

## Basic Usage

```jsx
import { Prompt, SystemContext } from 'xml-prompt';

const CodeReviewPrompt = ({ codeBlock }) => (
  <Prompt context="coding-assistant">
    <SystemContext role="programmer" />
    <Instruction>
      Review the following code and suggest improvements:
      {codeBlock}
    </Instruction>
  </Prompt>
);
```

## MDX Support

```mdx
# AI Assistant Prompt

<Prompt context="helpful-assistant">
  Answer user questions about {topic} clearly and concisely.
</Prompt>
```

## Component API

### `<Prompt>`
Root component for defining a complete prompt.

Props:
- `context`: (string) System context or role
- `children`: (node) Prompt content

### `<SystemContext>`
Defines the AI system's behavior and capabilities.

Props:
- `role`: (string) AI assistant role
- `constraints`: (array) Behavioral constraints

### `<UserInput>`
Placeholder for user input in prompt template.

Props:
- `format`: (string) Expected input format
- `validation`: (object) Input validation rules

## Examples

### Simple Prompt
```jsx
import { Prompt } from 'xml-prompt';

const SimplePrompt = () => (
  <Prompt context="general">
    Please explain the concept of {topic} in simple terms.
  </Prompt>
);
```

### Composed Prompt
```jsx
import { Prompt, SystemContext, UserInput, ResponseFormat } from 'xml-prompt';

const ComplexPrompt = () => (
  <PromptTemplate>
    <SystemContext role="expert" />
    <UserInput format="text" />
    <ResponseFormat type="structured" />
  </PromptTemplate>
);
```

## Benefits

- ✨ Familiar React/JSX syntax for prompt engineering
- 🔧 Component-based prompt composition
- ♻️ Enhanced prompt reusability
- 🎯 Clear separation of concerns
- 🛡️ Type safety with TypeScript support
- 🔄 Improved prompt maintenance
- 📝 Built-in documentation support via MDX

## Integration

Compatible with:
- React (>=16.8.0)
- Next.js
- MDX

## Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Maintainers

- [@likhonsdev](https://github.com/likhonsdev)

---

<div align="center">
Created with ❤️ by likhonsdev<br>
Last Updated: 2025-07-01 22:24:42 UTC
</div>
