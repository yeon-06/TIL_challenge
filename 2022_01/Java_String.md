### char[] vs String

๐ String์ char[]์ final๋ก ์ ์ธํ ๊ฒ์ผ๋ก ํธ๋ฆฌํ ๊ธฐ๋ฅ(๋ฉ์๋) ์ ๊ณต.

### String **str = โabcdโ** vs String **str = new String(โabcdโ)**

- `new ์์ฑ`: Java **Heap ์์ญ**์ ์๋ก์ด ๊ฐ์ฒด ํํ๋ก ์์ฑ
- `๋ฆฌํฐ๋ด ํ ๋น` : Java Heap ๋ฉ๋ชจ๋ฆฌ ๋ด๋ถ์ **String Pool**์ ์์ฑ

โ ๋ค๋ง new ํค์๋๋ฅผ ์ด์ฉํ์ด๋  `intern()` ๋ฉ์๋๋ฅผ ํตํด String Pool์ ๋ฑ๋ก ๊ฐ๋ฅ

### Immutable Object

= ๋ถ๋ณ ๊ฐ์ฒด

- ์์ฑ ํ ์ํ๋ฅผ ๋ณ๊ฒฝํ  ์ ์๋ ๊ฐ์ฒด
- ์์ฑ์, ์ ๊ทผ ๋ฉ์๋์ ๋ํด ๋ฐฉ์ด ๋ณต์ฌ๊ฐ ํ์ ์์
- ๊ฐ์ฒด๊ฐ ๊ฐ๋ ๊ฐ๋ง๋ค ์๋ก์ด ๊ฐ์ฒด ํ์
- ex: `String`, `Integer`, `Boolean` ๋ฑ

### String vs StringBuffer vs StringBuilder

|  | String | StringBuffer | StringBuilder |
| --- | --- | --- | --- |
| ๋ณ๊ฒฝ ๊ฐ๋ฅ | ๋ถ๋ณ | ๊ฐ๋ณ | ๊ฐ๋ณ |
| thread-safe | X | O | X |
| ๋ฌธ์์ด ์ถ๊ฐ | + | append() | append() |