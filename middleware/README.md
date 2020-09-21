# MIDDLEWARE

**This directory is not required, you can delete it if you don't want to use it.**

This directory contains your application middleware.
Middleware let you define custom functions that can be run before rendering either a page or a group of pages.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/guide/routing#middleware).


# The data:

I got the data from json generator:https://next.json-generator.com/NkO-Ahgrt

The information is like:
{
    Packaging: {
        products: [
          { 'repeat(5, 10)':{
                name: '{{company().toUpperCase()}}',
                price: '{{integer(100, 5000)}}',
                description: '{{lorem(2,"paragraphs" )}}',
                image: "https://picsum.photos/200",
                rate: '{{integer(0, 5)}}',
          } }
        ],
    },
          Furniture: {
        products: [
          { 'repeat(5, 10)':{
                name: '{{company().toUpperCase()}}',
                price: '{{integer(100, 5000)}}',
                description: '{{lorem(2,"paragraphs" )}}',
                image: "https://picsum.photos/200",
                rate: '{{integer(0, 5)}}',
          } }
        ],
    },
          Chemical: {
        products: [
          { 'repeat(5, 10)':{
                name: '{{company().toUpperCase()}}',
                price: '{{integer(100, 5000)}}',
                description: '{{lorem(2,"paragraphs" )}}',
                image: "https://picsum.photos/200",
                rate: '{{integer(0, 5)}}',
          } }
        ],
    }
        
}
