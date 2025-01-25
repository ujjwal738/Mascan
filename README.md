# React.js v19 + React-Canvas-Draw Integration

This project demonstrates the integration of **React.js v19** with the `react-canvas-draw` library to create a canvas drawing application. Users can draw freely on the canvas, clear their drawings, and even save or load them as JSON data for persistence.

---

## 🚀 Features

- **Freehand Drawing:** Draw directly on the canvas.
- **Save & Load Functionality:** Save your drawing as JSON and reload it anytime.
- **Clear Canvas:** Clear the canvas with a single click.
- **Modern React Setup:** Built with the latest React.js v19 features.

---

## 📦 Installation

Follow the steps below to set up and run the project locally:

### 1. Clone the Repository

```bash
git clone https://github.com/ujjwal738/assignment-intern.git
cd assignment-intern
```

### 2. Install Dependencies

```bash
npm install --legacy-peer-deps
```

> **Note:** The `--legacy-peer-deps` flag is required to resolve dependency conflicts between React v19 and `react-canvas-draw`, which is compatible with React 16.x or 17.x.

### 3. Start the Application

```bash
npm start
```

Open your browser and navigate to [http://localhost:3000](http://localhost:3000) to see the app in action.

---

## 🔗 Live Demo

Check out the live version of this project here: [Live Demo](https://ujjwal738.github.io/Mascan/)

---

## 🔧 Usage

1. **Draw on the Canvas:** Use your mouse or touchscreen to draw on the canvas.
2. **Save the Drawing:** Click the `Save` button to store your drawing as JSON.
3. **Load the Drawing:** Paste the saved JSON in the text area and click `Load` to restore the drawing.
4. **Clear the Canvas:** Click `Clear` to reset the canvas.

---

## 🛠️ Code Highlights

### **Key Libraries**

- [React.js v19](https://react.dev/) - A JavaScript library for building user interfaces.
- [react-canvas-draw](https://github.com/embiem/react-canvas-draw) - A lightweight library for canvas drawing in React applications.

### **Sample Code**

Here’s an example of how `react-canvas-draw` is used in this project:

```jsx
import React, { useRef } from "react";
import CanvasDraw from "react-canvas-draw";

const App = () => {
  const canvasRef = useRef(null);

  const saveDrawing = () => {
    const data = canvasRef.current.getSaveData();
    console.log("Saved Drawing Data:", data);
  };

  const loadDrawing = (data) => {
    canvasRef.current.loadSaveData(data, true);
  };

  return (
    <div>
      <h1>React Canvas Draw</h1>
      <CanvasDraw ref={canvasRef} />
      <button onClick={saveDrawing}>Save</button>
      <button onClick={() => loadDrawing(prompt("Paste JSON data here:"))}>Load</button>
      <button onClick={() => canvasRef.current.clear()}>Clear</button>
    </div>
  );
};

export default App;
```

---

## 🤝 Contributing

Contributions are welcome! If you encounter any issues or have feature requests, feel free to open an issue or create a pull request.

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

## 📚 Additional Resources

- [React.js Documentation](https://react.dev/)
- [react-canvas-draw GitHub Repository](https://github.com/embiem/react-canvas-draw)

---

## 🙌 Acknowledgments

Special thanks to the contributors of [react-canvas-draw](https://github.com/embiem/react-canvas-draw) for their awesome library!
