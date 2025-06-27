# React Native HTML Components

A comprehensive library of HTML-like components for React Native that allows you to write familiar HTML syntax while maintaining native performance and styling capabilities.

## 🚀 Features

- **Familiar HTML Syntax**: Use HTML-like components (`<Div>`, `<P>`, `<H1>`, etc.) in React Native
- **Tailwind CSS Support**: Full className support for Tailwind CSS styling
- **Native Performance**: Built on top of React Native's core components
- **TypeScript Ready**: Full TypeScript support with comprehensive type definitions
- **Semantic Elements**: Support for semantic HTML elements like `<Section>`, `<Article>`, `<Header>`
- **Form Components**: Complete form elements with native input handling
- **Table Support**: Full table structure components
- **Accessibility**: Built-in accessibility support following React Native best practices

## 📦 Installation

\`\`\`bash
npm install react-native-html-components
# or
yarn add react-native-html-components
\`\`\`

## 🎯 Quick Start

\`\`\`javascript
import React from 'react';
import { ScrollView } from 'react-native';
import { Div, H1, P, Button, Input, Card } from 'react-native-html-components';

export default function App() {
  return (
    <ScrollView>
      <Card>
        <H1 className="text-2xl font-bold text-center mb-4">
          Welcome to HTML Components
        </H1>
        <P className="text-gray-600 mb-4">
          Write React Native apps with familiar HTML syntax!
        </P>
        <Input 
          className="border border-gray-300 p-3 rounded mb-4"
          placeholder="Enter your name"
        />
        <Button 
          className="bg-blue-500 p-3 rounded"
          onPress={() => console.log('Hello!')}
        >
          <P className="text-white text-center font-semibold">Say Hello</P>
        </Button>
      </Card>
    </ScrollView>
  );
}
\`\`\`

## 📚 Available Components

### Block Elements
- `<Div>` - Generic container (View)
- `<Section>` - Section container
- `<Article>` - Article container
- `<Header>` - Header container
- `<Footer>` - Footer container
- `<Main>` - Main content container
- `<Nav>` - Navigation container

### Text Elements
- `<H1>` to `<H6>` - Headings with appropriate sizing
- `<P>` - Paragraph text
- `<Span>` - Inline text
- `<Strong>` - Bold text
- `<Em>` - Italic text
- `<Small>` - Small text
- `<Mark>` - Highlighted text
- `<Code>` - Inline code

### Form Elements
- `<Form>` - Form container
- `<Input>` - Text input
- `<Textarea>` - Multiline text input
- `<Button>` - Pressable button
- `<Label>` - Form labels
- `<Fieldset>` - Form field grouping
- `<Legend>` - Fieldset legend

### List Elements
- `<Ul>` - Unordered list
- `<Ol>` - Ordered list
- `<Li>` - List item
- `<Dl>` - Definition list
- `<Dt>` - Definition term
- `<Dd>` - Definition description

### Table Elements
- `<Table>` - Table container
- `<Thead>` - Table header
- `<Tbody>` - Table body
- `<Tr>` - Table row
- `<Th>` - Table header cell
- `<Td>` - Table data cell

### Media Elements
- `<Img>` - Image component
- `<Video>` - Video container
- `<Audio>` - Audio container

### Interactive Elements
- `<A>` - Link component with URL opening support

### Utility Elements
- `<Br>` - Line break
- `<Hr>` - Horizontal rule
- `<Card>` - Card container with shadow
- `<Container>` - Padded container
- `<Spacer>` - Flexible spacing component

### Quote Elements
- `<Blockquote>` - Block quotation
- `<Q>` - Inline quotation
- `<Cite>` - Citation

## 🎨 Styling

All components support both `className` (for Tailwind CSS) and `style` props:

\`\`\`javascript
// Using Tailwind classes
<Div className="bg-blue-500 p-4 rounded-lg shadow-md">
  <H1 className="text-white text-2xl font-bold">Styled with Tailwind</H1>
</Div>

// Using inline styles
<Div style={{ backgroundColor: '#3B82F6', padding: 16, borderRadius: 8 }}>
  <H1 style={{ color: 'white', fontSize: 24, fontWeight: 'bold' }}>
    Styled with inline styles
  </H1>
</Div>
\`\`\`

## 🔧 TypeScript Support

This library is written in TypeScript and provides comprehensive type definitions:

\`\`\`typescript
import { Div, H1, P, ButtonProps } from 'react-native-html-components';

interface CustomButtonProps extends ButtonProps {
  variant: 'primary' | 'secondary';
}

const CustomButton: React.FC<CustomButtonProps> = ({ variant, children, ...props }) => {
  const baseClass = variant === 'primary' ? 'bg-blue-500' : 'bg-gray-500';
  
  return (
    <Button className={`${baseClass} p-3 rounded`} {...props}>
      {children}
    </Button>
  );
};
\`\`\`

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License.
\`\`\`

```text file="LICENSE"
MIT License

Copyright (c) 2024 React Native HTML Components

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
