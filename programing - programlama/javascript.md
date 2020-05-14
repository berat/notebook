## Javascript

1. Randomly rewrite the existing object

``` javascript
const colors = {
    grey: '#BDC8D1',
    blue: '#0500FF',
    pink: '#FF00C7',
    orange: '#FF7A00',
};

const randomIndex = (arr) => (Math.random() * arr.length) >> 0;

const getRandom = (keys = [], times = 0, colors = []) => {
    if (!keys.length || times <= 0) {
        return colors;
    }

    const randIndex = randomIndex(keys);

    colors.push(keys[randIndex]);
    keys.splice(randIndex, 1);
    times--;

    return getRandom(keys, times, colors);
};
// colors will return random color up to length
console.log(getRandom(Object.keys(colors), Object.keys(colors).length)
```

2. Randomly rewrite the existing array

``` javascript
function shuffle(a) {
    for (let i = a.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [a[i], a[j]] = [a[j], a[i]];
    }
    return a;
}
```
