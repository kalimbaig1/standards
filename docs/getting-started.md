# Developer Runbook

This document provide instructions for the Developer for creating and adhering to coding and development standards is essential for ensuring code quaility !

---

## **Developer Coding Standard**
The standards help ensure that development practices are consistent, efficient, and produce high-quality software.

### **Naming Conventions**

* Use the meaningful and descriptive names

```bash
Classes
** Use PascalCase
Example MyClass, CustomerAccount,InvoiceDomain
Interfaces
Conventions: Use PascalCase, often prefixed with capital 'I' to denote an interface
```
For more details, see the [Developer Guide].
## **Code Formating sssssdfsdf sdfs df**
## **Code Formating**
* Indention rules
* Consistent use of brackets and braces
* Line Lenght
```bash
Example Indentiion rules

```

## **Commenting and Documentation**
* Write clear and Concise comments 
* Use Dcostring for function and class documentation 



## **Error Handling**
* Use try-catch blocks where apprropriate.
* Handle exceptions gracefully 
* Log errors with meaninghful message

## **Code Structure**

* Organize code into logical sections and modules 
* Follow the single responsbility principles.
* Avoid deep nesting and long methods.

```console
Standard Java Project Structure

my-java-project/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── example/
│   │   │           └── project/
│   │   │               ├── Application.java
│   │   │               ├── controller/
│   │   │               │   └── CustomerController.java
│   │   │               ├── model/
│   │   │               │   └── Customer.java
│   │   │               ├── repository/
│   │   │               │   └── CustomerRepository.java
│   │   │               ├── service/
│   │   │               │   └── CustomerService.java
│   │   │               └── config/
│   │   │                   └── AppConfig.java
│   │   └── resources/
│   │       ├── application.properties
│   │       └── logback.xml
│   └── test/
│       ├── java/
│       │   └── com/
│       │       └── example/
│       │           └── project/
│       │               ├── controller/
│       │               │   └── CustomerControllerTest.java
│       │               ├── model/
│       │               │   └── CustomerTest.java
│       │               ├── repository/
│       │               │   └── CustomerRepositoryTest.java
│       │               ├── service/
│       │               │   └── CustomerServiceTest.java
│       │               └── config/
│       │                   └── AppConfigTest.java
│       └── resources/
│           └── application-test.properties
├── pom.xml
└── README.md

Explanation
*	src/main/java: Contains the main application source code.
*	com/example/project/Application.java: The main class to run the application.
*	controller/: Contains REST controllers.
*	model/: Contains entity classes.
*	repository/: Contains repository interfaces.
*	service/: Contains service classes.
*	config/: Contains configuration classes.
•	src/main/resources: Contains resource files like properties, configuration, and static resources.
*	application.properties: Application configuration.
*	logback.xml: Logging configuration.
•	src/test/: Contains test source code.
*	src/test/java: Contains unit and integration tests.
*	src/test/resources: Contains test-specific resources.
•	pom.xml: Maven project file for managing dependencies and build configuration.
•	README.md: Project documentation.

```

## **Microservices Code Structure**
For a microservices architecture, each microservce is a separate, self contained project. Here's
a
```console
my-microservices-project/
│
├── customer-service/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── example/
│   │   │   │           └── customerservice/
│   │   │   │               ├── CustomerServiceApplication.java
│   │   │   │               ├── controller/
│   │   │   │               │   └── CustomerController.java
│   │   │   │               ├── model/
│   │   │   │               │   └── Customer.java
│   │   │   │               ├── repository/
│   │   │   │               │   └── CustomerRepository.java
│   │   │   │               ├── service/
│   │   │   │               │   └── CustomerService.java
│   │   │   │               └── config/
│   │   │   │                   └── AppConfig.java
│   │   └── resources/
│   │       ├── application.properties
│   │       └── logback.xml
│   └── test/
│       ├── java/
│       │   └── com/
│       │       └── example/
│       │           └── customerservice/
│       │               ├── controller/
│       │               │   └── CustomerControllerTest.java
│       │               ├── model/
│       │               │   └── CustomerTest.java
│       │               ├── repository/
│       │               │   └── CustomerRepositoryTest.java
│       │               ├── service/
│       │               │   └── CustomerServiceTest.java
│       │               └── config/
│       │                   └── AppConfigTest.java
│       └── resources/
│           └── application-test.properties
│   ├── pom.xml
│   └── README.md
│
├── order-service/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── example/
│   │   │   │           └── orderservice/
│   │   │   │               ├── OrderServiceApplication.java
│   │   │   │               ├── controller/
│   │   │   │               │   └── OrderController.java
│   │   │   │               ├── model/
│   │   │   │               │   └── Order.java
│   │   │   │               ├── repository/
│   │   │   │               │   └── OrderRepository.java
│   │   │   │               ├── service/
│   │   │   │               │   └── OrderService.java
│   │   │   │               └── config/
│   │   │   │                   └── AppConfig.java
│   │   └── resources/
│   │       ├── application.properties
│   │       └── logback.xml
│   └── test/
│       ├── java/
│       │   └── com/
│       │       └── example/
│       │           └── orderservice/
│       │               ├── controller/
│       │               │   └── OrderControllerTest.java
│       │               ├── model/
│       │               │   └── OrderTest.java
│       │               ├── repository/
│       │               │   └── OrderRepositoryTest.java
│       │               ├── service/
│       │               │   └── OrderServiceTest.java
│       │               └── config/
│       │                   └── AppConfigTest.java
│       └── resources/
│           └── application-test.properties
│   ├── pom.xml
│   └── README.md
│
├── api-gateway/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── example/
│   │   │   │           └── apigateway/
│   │   │   │               ├── ApiGatewayApplication.java
│   │   │   │               ├── config/
│   │   │   │               │   └── GatewayConfig.java
│   │   └── resources/
│   │       ├── application.properties
│   │       └── logback.xml
│   └── test/
│       ├── java/
│       │   └── com/
│       │       └── example/
│       │           └── apigateway/
│       │  
[          ]


```


Open up <http://127.0.0.1:8000/> in your browser, and you'll see the default
home page being displayed:

![The MkDocs live server](img/screenshot.png)

The dev-server also supports auto-reloading, and will rebuild your documentation
whenever anything in the configuration file, documentation directory, or theme
directory changes.

Open the `docs/index.md` document in your text editor of choice, change the
initial heading to `MkLorum`, and save your changes. Your browser will
auto-reload and you should see your updated documentation immediately.

Now try editing the configuration file: `mkdocs.yml`. Change the
[`site_name`][site_name] setting to `MkLorum` and save the file.

```yaml
site_name: MkLorum
```

Your browser should immediately reload, and you'll see your new site name take
effect.

![The site_name setting](img/site-name.png)

NOTE:
The [`site_name`][site_name] configuration
option is the only required option in your configuration file.

## Adding pages

Now add a second page to your documentation:

```bash
curl 'https://jaspervdj.be/lorem-markdownum/markdown.txt' > docs/about.md
```

As our documentation site will include some navigation headers, you may want to
edit the configuration file and add some information about the order, title, and
nesting of each page in the navigation header by adding a [`nav`][nav]
setting:

```yaml
site_name: MkLorum
nav:
  - Home: index.md
  - About: about.md
```

Save your changes and you'll now see a navigation bar with `Home` and `About`
items on the left as well as `Search`, `Previous`, and `Next` items on the
right.

![Screenshot](img/multipage.png)

Try the menu items and navigate back and forth between pages. Then click on
`Search`. A search dialog will appear, allowing you to search for any text on
any page. Notice that the search results include every occurrence of the search
term on the site and links directly to the section of the page in which the
search term appears. You get all of that with no effort or configuration on your
part!

![Screenshot](img/search.png)

## Theming our documentation

Now change the configuration file to alter how the documentation is displayed by
changing the theme. Edit the `mkdocs.yml` file and add a [`theme`][theme] setting:

```yaml
site_name: MkLorum
nav:
  - Home: index.md
  - About: about.md
theme: readthedocs
```

Save your changes, and you'll see the ReadTheDocs theme being used.

![Screenshot](img/readthedocs.png)

## Changing the Favicon Icon

By default, MkDocs uses the [MkDocs favicon] icon. To use a different icon, create
an `img` subdirectory in the `docs` directory and copy your custom `favicon.ico`
file to that directory. MkDocs will automatically detect and use that file as your
favicon icon.

[MkDocs favicon]: img/favicon.ico

## Building the site

That's looking good. You're ready to deploy the first pass of your `MkLorum`
documentation. First build the documentation:

```bash
mkdocs build
```

This will create a new directory, named `site`. Take a look inside the
directory:

```console
$ ls site
about  fonts  index.html  license  search.html
css    img    js          mkdocs   sitemap.xml
```

Notice that your source documentation has been output as two HTML files named
`index.html` and `about/index.html`. You also have various other media that's
been copied into the `site` directory as part of the documentation theme. You
even have a `sitemap.xml` file and `mkdocs/search_index.json`.

If you're using source code control such as `git` you probably don't want to
check your documentation builds into the repository. Add a line containing
`site/` to your `.gitignore` file.

```bash
echo "site/" >> .gitignore
```

If you're using another source code control tool you'll want to check its
documentation on how to ignore specific directories.

## Other Commands and Options

There are various other commands and options available. For a complete list of
commands, use the `--help` flag:

```bash
mkdocs --help
```

To view a list of options available on a given command, use the `--help` flag
with that command. For example, to get a list of all options available for the
`build` command run the following:

```bash
mkdocs build --help
```

## Deploying

The documentation site that you just built only uses static files so you'll be
able to host it from pretty much anywhere. Simply upload the contents of the
entire `site` directory to wherever you're hosting your website from and
you're done. For specific instructions on a number of common hosts, see the
[Deploying your Docs][deploy] page.

## Getting help

See the [User Guide] for more complete documentation of all of MkDocs' features.

To get help with MkDocs, please use the [GitHub discussions] or [GitHub issues].

[Installation Guide]: user-guide/installation.md
[docs_dir]: user-guide/configuration.md#docs_dir
[deploy]: user-guide/deploying-your-docs.md
[nav]: user-guide/configuration.md#nav
[GitHub discussions]: https://github.com/mkdocs/mkdocs/discussions
[GitHub issues]: https://github.com/mkdocs/mkdocs/issues
[site_name]: user-guide/configuration.md#site_name
[theme]: user-guide/configuration.md#theme
[User Guide]: user-guide/README.md
