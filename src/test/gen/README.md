# openapi-java-client

Bookstore API
- API version: 1.0.0
  - Build date: 2024-04-30T19:55:31.151827+01:00[Europe/London]

API for managing the bookstore's inventory, available authors, and customer orders


*Automatically generated by the [OpenAPI Generator](https://openapi-generator.tech)*


## Requirements

Building the API client library requires:
1. Java 1.8+
2. Maven (3.8.3+)/Gradle (7.2+)

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>org.openapitools</groupId>
  <artifactId>openapi-java-client</artifactId>
  <version>1.0.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
  repositories {
    mavenCentral()     // Needed if the 'openapi-java-client' jar has been published to maven central.
    mavenLocal()       // Needed if the 'openapi-java-client' jar has been published to the local maven repo.
  }

  dependencies {
     implementation "org.openapitools:openapi-java-client:1.0.0"
  }
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/openapi-java-client-1.0.0.jar`
* `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AuthorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8080/api/v1");

    AuthorApi apiInstance = new AuthorApi(defaultClient);
    try {
      apiInstance.authorsGet();
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthorApi#authorsGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}

```

## Documentation for API Endpoints

All URIs are relative to *http://localhost:8080/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthorApi* | [**authorsGet**](docs/AuthorApi.md#authorsGet) | **GET** /authors | List all authors
*AuthorApi* | [**authorsIdBooksGet**](docs/AuthorApi.md#authorsIdBooksGet) | **GET** /authors/{id}/books | List all books written by a specific author
*AuthorApi* | [**authorsIdDelete**](docs/AuthorApi.md#authorsIdDelete) | **DELETE** /authors/{id} | Delete an author
*AuthorApi* | [**authorsIdGet**](docs/AuthorApi.md#authorsIdGet) | **GET** /authors/{id} | Retrieve an author by their ID
*AuthorApi* | [**authorsIdPut**](docs/AuthorApi.md#authorsIdPut) | **PUT** /authors/{id} | Update an existing author
*AuthorApi* | [**authorsPost**](docs/AuthorApi.md#authorsPost) | **POST** /authors | Create a new author
*BooksApi* | [**booksGet**](docs/BooksApi.md#booksGet) | **GET** /books | List all books
*BooksApi* | [**booksISBNAuthorsGet**](docs/BooksApi.md#booksISBNAuthorsGet) | **GET** /books/{ISBN}/authors | List all authors of a book
*BooksApi* | [**booksISBNDelete**](docs/BooksApi.md#booksISBNDelete) | **DELETE** /books/{ISBN} | Delete a book
*BooksApi* | [**booksISBNGet**](docs/BooksApi.md#booksISBNGet) | **GET** /books/{ISBN} | Retrieve a book by ISBN
*BooksApi* | [**booksISBNOrdersGet**](docs/BooksApi.md#booksISBNOrdersGet) | **GET** /books/{ISBN}/orders | List all orders containing a specific book
*BooksApi* | [**booksISBNPut**](docs/BooksApi.md#booksISBNPut) | **PUT** /books/{ISBN} | Update an existing book
*BooksApi* | [**booksPost**](docs/BooksApi.md#booksPost) | **POST** /books | Create a new book
*OrdersApi* | [**ordersGet**](docs/OrdersApi.md#ordersGet) | **GET** /orders | List all orders
*OrdersApi* | [**ordersIdBooksGet**](docs/OrdersApi.md#ordersIdBooksGet) | **GET** /orders/{id}/books | List all books in an order
*OrdersApi* | [**ordersIdBooksISBNDelete**](docs/OrdersApi.md#ordersIdBooksISBNDelete) | **DELETE** /orders/{id}/books/{ISBN} | Remove a book from an existing order
*OrdersApi* | [**ordersIdBooksISBNPost**](docs/OrdersApi.md#ordersIdBooksISBNPost) | **POST** /orders/{id}/books/{ISBN} | Add a book to an existing order
*OrdersApi* | [**ordersIdGet**](docs/OrdersApi.md#ordersIdGet) | **GET** /orders/{id} | Retrieve an order by its ID
*OrdersApi* | [**ordersIdPut**](docs/OrdersApi.md#ordersIdPut) | **PUT** /orders/{id} | Update an existing order
*OrdersApi* | [**ordersPost**](docs/OrdersApi.md#ordersPost) | **POST** /orders | Create a new order


## Documentation for Models

 - [Author](docs/Author.md)
 - [Book](docs/Book.md)
 - [Order](docs/Order.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author



