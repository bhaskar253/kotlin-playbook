# Classes, Methods and Extension Functions

We tend to...

* Define data classes to represent the "platonic ideal" of a concept.  E.g. just the essential properties.

* Define fundamental operations as extension functions, [usually in the same file as the class](../organising-code/README.md).

* Define extension methods to avoid error-prone calls to the `copy` method of data classes.  These will also [usually be in the same file as the class](../organising-code/README.md)

* Define methods on the class only when required for object-oriented polymorphism.  E.g. to implement an interface, or to extend an abstract class.

* Define extension functions in other packages to relate the class to other concepts.  
  * For example, an "adapter" package for persistence of Articles as JSON blobs might define extension functions `Article.toJson(): JsonNode` and `JsonNode.toArticle(): Article`, and `Connection.loadArticle(id: ArticleId): Article?` and `Connection.saveArticle(article: Article)`.
