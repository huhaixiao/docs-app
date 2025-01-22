# navigator

## navigator.userAgent

- ios Safari设置请求桌面网站后 ua不会包含 iPhone iPad 关键字

## navigator.maxTouchPoints 

- 在PC下值为0
- 在PC仿真下值为1

## navigator.platform

### isiPad

```js
const isiPad = navigator.userAgent.match(/iPad/)
|| (navigator.platform === 'Macintosh'
&& navigator.maxTouchPoints > 1)
```