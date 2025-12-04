---
layout: essay
type: essay
title: "Beyond Libraries: An Introduction to Software Design Patterns"
date: 2025-12-04
published: true
labels:
  - Typescript 
  - Design Patterns
  - Software Engineering
---

<img width="400px" class="rounded float-end ps-4" src="../img/design-patterns.jpg">

## Introduction
When coding you will often encounter problems that are similar to ones that others have previously solved. Which is why libraries exist as well as design patterns but their functionality are different. Design patterns are like the skeletons of how to abstractly approach a problem, similar to dynamic programming where you need to work it out for a specific problem but there are general guides that you can follow. Which is unlike libraries where you can’t really modify them and they only work for the specific intention they were made with. 

## Types of Design Patterns
There are three categories of design patterns–creational, structural, and behavioral patterns. Creational design patterns are concerned with object creation mechanisms, increasing flexibility and reuse of code. Structural Patterns are concerned with composing classes and objects into larger structures. Behavioral Patterns are concerned with communication and interaction between objects.

## A Common Example of a Design Pattern
This website called <u>[Refactoring Guru](https://refactoring.guru/design-patterns/singleton/typescript/example#lang-features)</u> has a really good example of  Singleton in TypeScript:
```
/**
 * The Singleton class defines an `instance` getter, that lets clients access
 * the unique singleton instance.
 */
class Singleton {
    static #instance: Singleton;

    /**
     * The Singleton's constructor should always be private to prevent direct
     * construction calls with the `new` operator.
     */
    private constructor() { }

    /**
     * The static getter that controls access to the singleton instance.
     *
     * This implementation allows you to extend the Singleton class while
     * keeping just one instance of each subclass around.
     */
    public static get instance(): Singleton {
        if (!Singleton.#instance) {
            Singleton.#instance = new Singleton();
        }

        return Singleton.#instance;
    }

    /**
     * Finally, any singleton can define some business logic, which can be
     * executed on its instance.
     */
    public someBusinessLogic() {
        // ...
    }
}

/**
 * The client code.
 */
function clientCode() {
    const s1 = Singleton.instance;
    const s2 = Singleton.instance;

    if (s1 === s2) {
        console.log(
            'Singleton works, both variables contain the same instance.'
        );
    } else {
        console.log('Singleton failed, variables contain different instances.');
    }
}

clientCode();
```
### Output
The expected output of this code is “Singleton works, both variables contain the same instance.”

### Explanation
This example can be used for managing resources like data connections, configuration settings, or centralized logging services where having multiple instances would lead to inconsistencies or resource waste. Basically it uses encapsulation and static properties to guarantee that regardless of how many times the instance getter is accessed, only one object of the Singleton class ever exists.

## Design Pattern in Final Project
There were a few design patterns that were used in my group’s final project but the one that I noticed was a **Structural Design Pattern**. Which can be shown in [src/app/layout.tsx](https://github.com/RI-Bows/RIBows/blob/main/src/app/layout.tsx) and and is an example of the **Template Method-Style Structural pattern**:
```
export const metadata: Metadata = {
  title: 'RIBows',
  description: 'RIOs for the University of Hawaii Community',
};

export default function RootLayout({
  children,
}: Readonly<{
  children: React.ReactNode;
}>) {
  const classString = `${inter.className} wrapper`;
  return (
    <html lang="en">
      <body className={classString}>
        <Providers>
          <NavBar />
          {children}
          <Footer />
        </Providers>
      </body>
    </html>
  );
}
``` 
This file acts as a structural template for the entire application. The html and body tags, along with global elements like NavBar, Providers, and Footer, form a fixed outer layout that every page inherits. The {children} prop serves as the “hook” where page-specific content is inserted. This separation—a stable outer structure with interchangeable inner content—is the defining characteristic of a structural pattern. It organizes how components fit together, enforces consistent layout across all pages, and mirrors the Template Method design pattern by establishing a reusable framework while allowing individual pages to supply variable content.

## Conclusion
Overall, exploring design patterns helped me recognize how experienced developers approach recurring software challenges. Seeing these ideas applied not just in tutorials but also within my own project such as the structural Template Method pattern in our layout, made the concepts feel much more concrete. This understanding will influence how I design and organize my code in future projects, encouraging me to think more intentionally about structure, reuse, and maintainability.