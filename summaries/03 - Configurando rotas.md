# Configurando rotas

Crie o arquivo routes.js

Instale o react-router-dom

```
yarn add react-router-dom
```

Crie a estrutura de pastas dentro de src.

    -src
      -pages
        -Cart
          index.js
        -Home
          index.js

routes.js

```js
import React from 'react';
import { Switch, Route } from 'react-router-dom';

import Home from './pages/Home/index';
import Cart from './pages/Cart/index';

export default function Routes() {
  return (
    <Switch>
      <Route path="/" exact component={Home} />
      <Route path="/cart" exact component={Cart} />
    </Switch>
  );
}
```

#### Dica: _Digite rfc com o plugin da Rocket para criar um componente funcional_

Home/index.js

```js
import React from 'react';

// import { Container } from './styles';

export default function Home() {
  return <h1>Home</h1>;
}
```

Cart/index.js

```js
import React from 'react';

// import { Container } from './styles';

export default function Cart() {
  return <h1>Carrinho</h1>;
}
```

App.js

```js
import React from 'react';
import { BrowserRouter } from 'react-router-dom';
import Routes from './routes';

function App() {
  return (
    <BrowserRouter>
      <Routes />
    </BrowserRouter>
  );
}

export default App;
```
