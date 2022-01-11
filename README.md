Imagine you have this array:

```js
[
   { title: 'war of the worlds', author: 'wells', genre: 'scifi' }, 
   { title: 'pride and prejudice', author: 'austen', genre: 'classic' }, 
   { title: 'sula', author: 'morrison', genre: 'classic' },
   { title: 'the road', author: 'mccarthy', genre: 'scifi' } 
]
```

## .map

We can get an array just the titles as strings like so:

`books.map(book => book.title)`

We can make an array of `{ writer, work }` objects (that is, changing the names of keys), like so:

```js
books.map(book => {
     return { 
        writer: book.author,
        work: book.title
     }
})
```

## .filter

We can get an array of just classic books as objects like so:

`books.filter(book => book.genre === 'classic')`

## .filter then .map

Array methods can be chained together.

We can get an array of just scifi titles as strings like so:

```js
books
  .filter(book => book.genre === 'classic')
  .map(book => book.title)
```

