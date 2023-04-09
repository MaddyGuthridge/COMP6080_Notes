A styled component is a [[React]] [[component]] with additional [[CSS]] styling. This is preferable to [[raw CSS in React]] as it doesn't have namespace pollution issues.

## In material UI
```jsx
import { styled } from '@mui/system';

const BigButton = styled(Button)({
  width: '200px',
});
```