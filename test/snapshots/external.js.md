# Snapshot report for `test/external.js`

The actual snapshot is saved in `external.js.snap`.

Generated by [AVA](https://ava.li).

## (optimized) transpiles external stylesheets

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    import colors, { size } from './constants';␊
    const color = 'red';␊
    const zzz = ["div[jsx-3567928963] {\\n  font-size: 3em;\\n  animation: fadeIn-jsx-3567928963 3s ease-in forwards;\\n}", "@keyframes fadeIn-jsx-3567928963 {\\n  0% {\\n    opacity: 0;\\n  }\\n\\n  100% {\\n    opacity: 1;\\n  }\\n}", "@media (min-width: 480px) {\\n  div[jsx-3567928963] {\\n    color: red;\\n  }\\n}"];␊
    zzz.__hash = "3567928963";␊
    const bar = ["div[jsx-2141779268] {\\n  font-size: 3em;\\n}"];␊
    bar.__hash = "2141779268";␊
    const baz = ["div {\\n  font-size: 3em;\\n}"];␊
    baz.__hash = "2141779268";␊
    a.__hash = "262929833";␊
    const a = [`div {␊
      font-size: ${size}em;␊
    }`];␊
    export const uh = bar;␊
    export const foo = [`div[jsx-2433716433] {␊
      color: ${color};␊
    }`];␊
    foo.__hash = "2433716433";␊
    ({␊
      styles: <_JSXStyle id={"1329679275"}>{[`div[jsx-1329679275] {␊
      color: ${colors.green.light};␊
    }`, "a[jsx-1329679275] {\\n  color: red;\\n}"]}</_JSXStyle>,␊
      className: "jsx-1329679275"␊
    });␊
    const b = {␊
      styles: <_JSXStyle id={"1329679275"}>{[`div[jsx-1329679275] {␊
      color: ${colors.green.light};␊
    }`, "a[jsx-1329679275] {\\n  color: red;\\n}"]}</_JSXStyle>,␊
      className: "jsx-1329679275"␊
    };␊
    ␊
    const dynamic = colors => {␊
      const b = {␊
        styles: <_JSXStyle id={"3325296745"} dynamic={[colors.green.light]}>{[`div[__jsx-style-dynamic-selector] {␊
      color: ${colors.green.light};␊
    }`, "a[__jsx-style-dynamic-selector] {\\n  color: red;\\n}"]}</_JSXStyle>,␊
        className: _JSXStyle.dynamic([["3325296745", [colors.green.light]]])␊
      };␊
    };␊
    ␊
    export default {␊
      styles: <_JSXStyle id={"3290112549"}>{["div[jsx-3290112549] {\\n  font-size: 3em;\\n}", `p[jsx-3290112549] {␊
      color: ${color};␊
    }`]}</_JSXStyle>,␊
      className: "jsx-3290112549"␊
    };`

## (optimized) transpiles external stylesheets (CommonJS modules)

> Snapshot 1

    `const _defaultExport = ["div[jsx-2292456818] {\\n  font-size: 3em;\\n}"];␊
    _defaultExport.__hash = "2292456818";␊
    module.exports = _defaultExport;`

## Makes sure that style nodes are not re-used

> Snapshot 1

    `"use strict";␊
    ␊
    var _style = _interopRequireDefault(require("styled-jsx/style"));␊
    ␊
    var _App = _interopRequireDefault(require("./App.styles"));␊
    ␊
    function _interopRequireDefault(obj) { return obj && obj.__esModule ? obj : { default: obj }; }␊
    ␊
    function Test() {␊
      return <div>␊
            <_style.default id={_App.default.__hash}>{_App.default}</_style.default>␊
          </div>;␊
    }`

## does not transpile non-styled-jsx tagged teplate literals

> Snapshot 1

    `import css from 'hell';␊
    const color = 'red';␊
    const bar = css`␊
      div {␊
        font-size: 3em;␊
      }␊
    `;␊
    export const uh = bar;␊
    export const foo = css`div { color: ${color}}`;␊
    export default css`␊
      div {␊
        font-size: 3em;␊
      }␊
      p {␊
        color: ${color};␊
      }␊
    `;␊
    const Title = styled.h1`␊
      color: red;␊
      font-size: 50px;␊
    `;␊
    const AnotherTitle = Title.extend`color: blue;`;␊
    export const Component = () => <AnotherTitle>My page</AnotherTitle>;`

## injects JSXStyle for nested scope

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    ␊
    function test() {␊
      ({␊
        styles: <_JSXStyle id={"2886504620"}>{"div[jsx-2886504620] { color: red\\n}"}</_JSXStyle>,␊
        className: "jsx-2886504620"␊
      });␊
    }`

## transpiles external stylesheets

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    import colors, { size } from './constants';␊
    const color = 'red';␊
    const zzz = new String("\\ndiv[jsx-3567928963] {\\n    font-size: 3em;\\n    animation: fadeIn-jsx-3567928963 3s ease-in forwards;\\n}\\n@keyframes fadeIn-jsx-3567928963 {\\n0% {\\n      opacity: 0;\\n}\\n100% {\\n      opacity: 1;\\n}\\n}\\n@media (min-width: 480px) {\\ndiv[jsx-3567928963] {\\n      color: red;\\n}\\n}\\n");␊
    zzz.__hash = "3567928963";␊
    const bar = new String("\\ndiv[jsx-2141779268] {\\n    font-size: 3em;\\n}\\n");␊
    bar.__hash = "2141779268";␊
    const baz = new String("\\n  div {\\n    font-size: 3em;\\n  }\\n");␊
    baz.__hash = "2141779268";␊
    a.__hash = "262929833";␊
    const a = new String(`␊
      div {␊
        font-size: ${size}em;␊
      }␊
    `);␊
    export const uh = bar;␊
    export const foo = new String(`␊
    div[jsx-2433716433] {␊
        color: ${color};␊
    }␊
    `);␊
    foo.__hash = "2433716433";␊
    ({␊
      styles: <_JSXStyle id={"1329679275"}>{`␊
    div[jsx-1329679275] {␊
        color: ${colors.green.light};␊
    }␊
    a[jsx-1329679275] { color: red␊
    }␊
    `}</_JSXStyle>,␊
      className: "jsx-1329679275"␊
    });␊
    const b = {␊
      styles: <_JSXStyle id={"1329679275"}>{`␊
    div[jsx-1329679275] {␊
        color: ${colors.green.light};␊
    }␊
    a[jsx-1329679275] { color: red␊
    }␊
    `}</_JSXStyle>,␊
      className: "jsx-1329679275"␊
    };␊
    ␊
    const dynamic = colors => {␊
      const b = {␊
        styles: <_JSXStyle id={"3325296745"} dynamic={[colors.green.light]}>{`␊
    div[__jsx-style-dynamic-selector] {␊
          color: ${colors.green.light};␊
    }␊
    a[__jsx-style-dynamic-selector] { color: red␊
    }␊
      `}</_JSXStyle>,␊
        className: _JSXStyle.dynamic([["3325296745", [colors.green.light]]])␊
      };␊
    };␊
    ␊
    export default {␊
      styles: <_JSXStyle id={"3290112549"}>{`␊
    div[jsx-3290112549] {␊
        font-size: 3em;␊
    }␊
    p[jsx-3290112549] {␊
        color: ${color};␊
    }␊
    `}</_JSXStyle>,␊
      className: "jsx-3290112549"␊
    };`

## transpiles external stylesheets (CommonJS modules)

> Snapshot 1

    `const _defaultExport = new String("\\ndiv[jsx-2292456818] { font-size: 3em\\n}\\n");␊
    ␊
    _defaultExport.__hash = "2292456818";␊
    module.exports = _defaultExport;`

## use external stylesheet and dynamic element

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    import styles from './styles2';␊
    export default (({␊
      level = 1␊
    }) => {␊
      const Element = `h${level}`;␊
      return <Element className="root" {...{␊
        [`jsx-${styles.__hash}`]: ""␊
      }}>␊
          <p {...{␊
          [`jsx-${styles.__hash}`]: ""␊
        }}>dynamic element</p>␊
          <_JSXStyle id={styles.__hash}>{styles}</_JSXStyle>␊
        </Element>;␊
    });`

## use external stylesheets

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    import styles from './styles';␊
    ␊
    const styles2 = require('./styles2');␊
    ␊
    import { foo as styles3 } from './styles';␊
    export default (() => <div {...{␊
      [`jsx-${styles3.__hash}`]: "",␊
      [`jsx-${styles.__hash}`]: "",␊
      ["jsx-1646697228"]: ""␊
    }}>␊
        <p className="foo" {...{␊
        [`jsx-${styles3.__hash}`]: "",␊
        [`jsx-${styles.__hash}`]: "",␊
        ["jsx-1646697228"]: ""␊
      }}>test</p>␊
        <p {...{␊
        [`jsx-${styles3.__hash}`]: "",␊
        [`jsx-${styles.__hash}`]: "",␊
        ["jsx-1646697228"]: ""␊
      }}>woot</p>␊
        <_JSXStyle id={styles2.__hash}>{styles2}</_JSXStyle>␊
        <_JSXStyle id={styles3.__hash}>{styles3}</_JSXStyle>␊
        <div {...{␊
        [`jsx-${styles3.__hash}`]: "",␊
        [`jsx-${styles.__hash}`]: "",␊
        ["jsx-1646697228"]: ""␊
      }}>woot</div>␊
        <_JSXStyle id={"1646697228"}>{"\\np[jsx-1646697228] {\\n        color: red;\\n}\\ndiv[jsx-1646697228] {\\n        color: green;\\n}\\n    "}</_JSXStyle>␊
        <_JSXStyle id={styles.__hash}>{styles}</_JSXStyle>␊
      </div>);␊
    export const Test = () => <div {...{␊
      [`jsx-${styles3.__hash}`]: "",␊
      ["jsx-1646697228"]: ""␊
    }}>␊
        <p className="foo" {...{␊
        [`jsx-${styles3.__hash}`]: "",␊
        ["jsx-1646697228"]: ""␊
      }}>test</p>␊
        <p {...{␊
        [`jsx-${styles3.__hash}`]: "",␊
        ["jsx-1646697228"]: ""␊
      }}>woot</p>␊
        <_JSXStyle id={styles3.__hash}>{styles3}</_JSXStyle>␊
        <div {...{␊
        [`jsx-${styles3.__hash}`]: "",␊
        ["jsx-1646697228"]: ""␊
      }}>woot</div>␊
        <_JSXStyle id={"1646697228"}>{"\\np[jsx-1646697228] {\\n        color: red;\\n}\\ndiv[jsx-1646697228] {\\n        color: green;\\n}\\n    "}</_JSXStyle>␊
      </div>;`

## use external stylesheets (global only)

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    import styles, { foo as styles3 } from './styles';␊
    ␊
    const styles2 = require('./styles2');␊
    ␊
    export default (() => <div>␊
        <p>test</p>␊
        <div>woot</div>␊
        <p>woot</p>␊
        <_JSXStyle id={styles2.__hash}>{styles2}</_JSXStyle>␊
        <_JSXStyle id={styles3.__hash}>{styles3}</_JSXStyle>␊
        <_JSXStyle id={styles.__hash}>{styles}</_JSXStyle>␊
      </div>);`

## use external stylesheets (multi-line)

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    import styles from './styles';␊
    export default (() => <div {...{␊
      [`jsx-${styles.__hash}`]: ""␊
    }}>␊
        <p {...{␊
        [`jsx-${styles.__hash}`]: ""␊
      }}>test</p>␊
        <_JSXStyle id={styles.__hash}>{styles}</_JSXStyle>␊
      </div>);`