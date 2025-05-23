# Wiggle Bones with React Three Fiber

A dynamic 3D animation project implementing the Wiggle Bones library with React Three Fiber and Three.js.

![Wiggle Bones](/public/md.png)

## 🌟 Overview

This project demonstrates how to implement physics-based secondary animations using the Wiggle Bones library in React Three Fiber. Create natural, springy movements for characters, objects, and environments that respond realistically to movement and interactions.

## ✨ Features

- **Physics-Based Secondary Animations**: Add natural, springy movements to 3D models
- **Customizable Parameters**: Fine-tune stiffness, damping, and mass for perfect motion
- **3D Model Integration**: Works with Mixamo animated character models
- **Performance Optimized**: Efficient implementation for smooth framerates
- **React Three Fiber Integration**: Seamlessly works within the R3F ecosystem

## 🛠️ Tech Stack

- React
- Three.js
- React Three Fiber
- Wiggle Bones Library
- Mixamo for character animations

## 📝 Usage Guide

### Basic Setup

```jsx
import { WiggleRoot, WiggleBone } from 'wiggle-bones-react';

function MyModel() {
  return (
    <WiggleRoot>
      <mesh>
        <boxGeometry />
        <meshStandardMaterial />
        <WiggleBone 
          stiffness={0.3}
          damping={0.8}
          mass={1}
        />
      </mesh>
    </WiggleRoot>
  );
}
```

### Working with Mixamo Models

1. Download an animated character from Mixamo
2. Import the model into your project
3. Wrap the desired bones with WiggleBone components
4. Adjust parameters to achieve the desired effect

```jsx
<WiggleBone 
  boneId="mixamorigHair"
  stiffness={0.4}
  damping={0.7}
  mass={1.2}
  gravityMultiplier={0.5}
/>
```

## 🧩 Key Components

### WiggleRoot

The container component that initializes the Wiggle system.

### WiggleBone

Applied to individual bones or objects to create springy, physics-based movements.

### Parameters Explained

- **stiffness**: Controls how rigid the spring is (0-1)
- **damping**: Controls how quickly oscillations settle (0-1)
- **mass**: Affects how responsive the bone is to forces
- **gravityMultiplier**: How much gravity affects the bone

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
