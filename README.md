# @team-by-team/react-drawer

## Installation

```bash
# npm
npm i @team-by-team/react-drawer

# yarn
yarn add @team-by-team/react-drawer

# pnpm
pnpm add @team-by-team/react-drawer

# bun
bun add @team-by-team/react-drawer
```

## Basic usage

```tsx
() => {
  const [isOpen, setIsOpen] = useState(false);

  const handleOpen = () => {
    setIsOpen(() => true);
  };

  const handleClose = () => {
    setIsOpen(() => false);
  };

  return (
    <>
      <button onClick={handleOpen}>Open Drawer</button>
      <Drawer isOpen={isOpen} onClose={handleClose}>
        <h1>Drawer</h1>
      </Drawer>
    </>
  );
};
```

## Placement

```tsx
() => {
  const [isOpen, setIsOpen] = useState(false);
  const placement = 'top'; // 'top' | 'right' | 'bottom' | 'left'

  const handleOpen = () => {
    setIsOpen(() => true);
  };

  const handleClose = () => {
    setIsOpen(() => false);
  };

  return (
    <>
      <button onClick={handleOpen}>Open Drawer</button>
      <Drawer isOpen={isOpen} onClose={handleClose}>
        <h1>Drawer</h1>
      </Drawer>
    </>
  );
};
```

## Size

```tsx
() => {
  const [isOpen, setIsOpen] = useState(false);
  const size = 'large'; // 'default' | 'large'

  const handleClose = () => {
    setIsOpen(() => false);
  };

  return (
    <Drawer isOpen={isOpen} onClose={handleClose} size={size}>
      <h1>Drawer</h1>
    </Drawer>
  );
};
```

## Customize transition duration

```tsx
() => {
  const [isOpen, setIsOpen] = useState(false);
  const transitionDurationMS = 500; // Customized duration

  const handleClose = () => {
    setIsOpen(() => false);
  };

  return (
    <Drawer
      isOpen={isOpen}
      onClose={handleClose}
      transitionDurationMS={transitionDurationMS}
    >
      <h1>Drawer</h1>
    </Drawer>
  );
};
```

## Props

`children`

- Components to be rendered inside the Drawer (Header, content, close button, etc.)
- Type : `React.ReactNode`

`isOpen`

- Indicates whether the Drawer is visible on the screen.
- Type : `boolean`
- default: `false`

`onClose`

- Function to be executed when the Drawer is closed.
- Type : `() => void`

`placement` (optional)

- Specifies the position where the Drawer will appear.
- Type : `'top' | 'right' | 'bottom' | 'left'`
- Default : `'right'`

`size` (optional)

- Size of the Drawer.
- Type : `'default' | 'large'`
- Default : `'default'`

`width` (optional)

- Width of the Drawer.
- Type : `React.CSSProperties['width']`

`height` (optional)

- Height of the Drawer.
- Type : `React.CSSProperties['height']`

`transitionDurationMS` (optional)

- Duration of the animation when the Drawer opens and closes.
- Type : `number`
- Default : `300`

`zIndex` (optional)

- Value for the z-index property of the Drawer.
- Type : `number`
- Default : `1000`

`css` (optional)

- Style object containing additional CSS properties to be applied.
- Type : `CSSInterpolation`
