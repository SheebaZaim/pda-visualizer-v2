

# 🎓 Pushdown Automata Visualizer

An interactive web-based tool for visualizing and simulating Pushdown Automata (PDAs). Perfect for students learning formal languages and automata theory!

## 🌟 Features

- **Interactive State Editor**: Create and manage PDA states with ease
- **Visual Transition Designer**: Define transitions with read/pop/push operations
- **Real-time Simulation**: Watch your PDA execute step-by-step
- **Animated Visualizations**: 
  - State diagram with highlighted current state
  - Stack animation showing push/pop operations
  - Input tape with position tracking
- **Pre-loaded Examples**: 
  - Balanced Parentheses
  - aⁿbⁿ Language
  - Palindromes (odd length)
- **Save/Load Configurations**: Export your PDAs as JSON

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ installed on your system
- npm, yarn, or pnpm package manager

### Installation

1. **Clone or create the project:**
```bash
npx create-next-app@latest pda-visualizer --typescript --tailwind --app
cd pda-visualizer
```

2. **Install dependencies:**
```bash
npm install lucide-react
```

3. **Copy all the files** from the project structure into your `src/` directory

4. **Run the development server:**
```bash
npm run dev
```

5. **Open your browser:**

Navigate to [http://localhost:3000](http://localhost:3000)

## 📖 How to Use

1. **Load an Example**: Click on one of the example PDAs to get started
2. **Define States**: Add states and mark start/accept states
3. **Create Transitions**: Specify (read, pop, push) rules for each transition
4. **Enter Input**: Type your test string
5. **Initialize**: Click "Initialize PDA" to prepare the simulation
6. **Simulate**: 
   - Use "Step Forward" for manual step-by-step execution
   - Use "Play All" for automatic simulation
   - Use "Reset" to go back to the initial state

## 🎯 Example PDAs

### Balanced Parentheses
- **Language**: `L = { w | w has balanced parentheses }`
- **Test**: `()()` ✅ | `(()` ❌

### aⁿbⁿ
- **Language**: `L = { aⁿbⁿ | n ≥ 1 }`
- **Test**: `aabb` ✅ | `aaab` ❌

### Palindrome (Odd Length)
- **Language**: `L = { wcwᴿ | w ∈ {a,b}* }`
- **Test**: `abcba` ✅ | `abcd` ❌

## 🛠️ Tech Stack

- **Framework**: Next.js 14 with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Visualization**: HTML5 Canvas API

## 📁 Project Structure
````
src/
├── app/
│   ├── layout.tsx          # Root layout
│   ├── page.tsx            # Main page
│   └── globals.css         # Global styles
├── components/
│   ├── PDAVisualizer.tsx   # Main component
│   ├── StateEditor.tsx     # State management UI
│   ├── TransitionEditor.tsx # Transition definition UI
│   ├── StackVisualizer.tsx # Stack animation
│   ├── InputTape.tsx       # Input display
│   └── StateDiagram.tsx    # State graph visualization
├── engine/
│   ├── PDAEngine.ts        # Core PDA logic
│   └── Stack.ts            # Stack data structure
├── types/
│   └── pda.types.ts        # TypeScript interfaces
└── utils/
    └── examples.ts         # Pre-defined PDAs