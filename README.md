##
The `async` keyword

- Async keyword always return a promise.
- If the function returns a value, the promise will be resolved with that value.
- If the function throws an exception, the promise will be rejected.

```
const delayedColorChange = (color, delay) => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            document.body.style.backgroundColor = color;
            resolve();
        }, delay)
    })
}

```

```
async function rainbow() {
    await delayedColorChange('red', 1000)
    await delayedColorChange('orange', 1000)
    await delayedColorChange('yellow', 1000)
    await delayedColorChange('green', 1000)
    await delayedColorChange('blue', 1000)
    await delayedColorChange('indigo', 1000)
    await delayedColorChange('violet', 1000)
    return "ALL DONE!"
}
```

## [Click for the dev tools console](https://verson-tech.github.io/AsyncFunctions/)

Lisence: 'The Web Developer Bootcamp 2022' (UDEMY)