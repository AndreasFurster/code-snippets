# JS Snippets
## Named console log

    const superlog = (name) => (...args) => console.log(name, ...args)

Example usage:

    $('.element').on('click', superlog('onclick')) // => onclick [eventargs]
