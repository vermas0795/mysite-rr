---
title: "Coding Standards"
description: " Coding standards is a very important aspect of any programming language. And every organization must have a well-defined and standard style of coding that should be followed by everyone within the organization"
date: 2020-01-28T00:34:51+09:00
draft: false
weight: -4
---
![RR-Logo](../../../images/Rolls-Royce.jpg)

### Coding Standards

Version 1.0

![R2DL-Logo](../../../images/R2DL.jpg)

**Warning**

This is a hard copy of a document maintained on electronic media. It may not be the latest version. Kindly ascertain the latest version from the Document Master List available with the Project Leader.

**REVISION LIST**

| Revision No. | Revision Date | Revision Description | Revision By | Remarks |
| - | - | - | - | - |
| Initial Draft | 12/06/2020 | Initial Setup | Samitanjaya Mishra |   |
| v0.1 | 08/07/2020 | Review Comment Implemented | Samitanjaya Mishra |   |

**REVIEW LIST**

| Revision No. | Revision Date | Revision By | Remarks |
| - | - | - | - |
| Initial Draft | 04/06/2020 | Mayank Madhukar |   |
| v0.1 | 10/07/2020 | Mayank Madhukar |   |

## 1. Introduction

This sections details the overall purpose of the document, the target audience who can refer the document and the references used while creating this document.

### 1.1 Purpose

> This document is the guideline that can be followed as a base for any type of project in any of the stream and projects. Coding standards is a very important aspect of any programming language. And every organization must have a well-defined and standard style of coding that should be followed by everyone within the organization. The purpose of this document is to serve the very purpose of defining certain coding standards and guidelines that suit best for the organization based on the type of software's being developed.

### 1.2 Intended Audience

This document is intended for the following audience:

- **Development Teams** -- As a reference for development team for maintaining certain guidelines while writing code for any project.

## 2. Common Standards

A coding standard provides a uniform appearance to the code developed by different engineers. It improves readability and maintainability of the code and it reduces the complexity too. It promotes sound programming practices and increases efficiency of the programmers.

Some of the common coding standards are given below:

a.  **Naming Conventions:**

- Variable names should be meaningful and understandable, so that it would be helpful for anyone to understand the reason for using it.
- Camel casing should be used for naming local variables(**e.g. userName**), Global variables should start with the capital letter(**e.g. SessionId**) and Constant names should be filled using capital letters only(**e.g. CONSTDATA**).
- It is advisable to avoid the use of digits in a variable name.
- Function name should always be written in UpperCamelCase(**e.g.GetEmployee**).
- Function name should describe the use of the function briefly and clearly.

b.  **Indentation:**

> Proper Indentation is very important to increase the readability of the code.
> 
> White spaces should be used properly by the programmers to make the code readable. Please find the spacing conventions below:

- There must be a space after giving a comma between two function arguments.
- Each nested block should be properly indented and spaced.
- There should proper indentation at the beginning and ending of each block.
- All braces should start from a new line and the code following end of braces should also start from a new line.

c.  **Error return values and exception handling:**

> Functions encountering an error condition should return either 0 or 1 for simplifying debugging. Functions containing any exception throwing statements should be handled properly using appropriate Exception Handling code.

d.  **Avoiding complex coding styles:**

> Code should be easily understandable. Complex code makes maintenance and debugging difficult and expensive.

e.  **Code should be well documented:**

> The code should be properly commented and proper method documentation should be provided to increase the understandability of the code.

f.  **Avoid lengthy functions:**

> Lengthy functions are difficult to understand. Functions should be small enough to carry out small work and lengthy functions should be broken into small ones for completing small tasks.

## 3. C-Sharp Coding Best Practices

### 3.1 Naming Conventions and Standards

Below are the C# coding standards, naming conventions, and best practices.

- use**PascalCasing** for class names and method names.

> public class **TotalSale**
> 
> {
> 
> public void **CalculateIndividuals()**
> 
> //...
> 
> }
> 
> }

- use**camelCasing** for method arguments and local variables.

> public class TotalSale
> 
> {
> 
> public void CalculateIndividuals()
> 
> {
> 
> int **itemCount** = //Logic
> 
> }
> 
> }

- do not use**Hungarian** notation or any other type identification in identifiers.

> **//correct**
> 
> **string department;**
> 
> **int counter;**
> 
> **//avoid**
> 
> string strDepartment;
> 
> int iCounter;

- avoid using**Abbreviations**. Exceptions: abbreviations commonly used as names, such as**Id, Xml, Ftp, Uri**

> //correct
> 
> UserGroup userGroup;
> 
> //avoid
> 
> UserGroup usrGrp;
> 
> //Exception
> 
> CustomerId customerId

- do not use**Screaming Caps** for constants or readonly variables

> //correct
> 
> public static string ShippingType = "Cargo Ship"
> 
> //Avoid
> 
> public static string SHIPPINGTYPE="Cargo Ship"

- do not use**Underscores** in identifiers. Exception: you can prefix private static variables with an underscore.

> //correct
> 
> public DateTime clientAppointment;
> 
> //Avoid
> 
> public DateTime client_Appointment;

- use**predefined type names** instead of system type names like Int16, Single, UInt64, etc.

> //correct
> 
> string firstName;
> 
> //Avoid
> 
> String firstName;

- use implicit type**var** Exception: primitive types (int, string, double, etc) use predefined names. for local variable declarations.

> //correct
> 
> var stream = File.Create(path);
> 
> //exceptions
> 
> Int index = 1;

- use noun or noun phrases to name a class.

> //correct
> 
> public class BusniessLocation

- prefix interfaces with the letter**I**.  Interface names are noun (phrases) or adjectives.

> //correct
> 
> interface IShape

- name source files according to their main classes. Exception: file names with partial classes reflect their source or purpose, e.g designer, generated, etc declare all member variables at the top of a class, with static variables at the very top.
- use singular names for enums. Exception: bit field enums.
- explicitly specify a type of an enum or values of enums (except bit fields).
- use TAB for indentation. Do not use SPACES. Define the Tab size as 4. Comments should be in the same level as the code (use the same level of indentation).
- use of SOLID Principles and Design Patterns should be more emphasized.
  
### 3.2 Performance Enhancements

> To Be Continued...

### 3.3 Exception Handling

- **Use try/catch/finally blocks to recover from errors or release resources**

> Use try/catch blocks around code that can potentially generate an exception and your code can recover from that exception. In catch blocks, always order exceptions from the most derived to the least derived.

- **Handle common conditions without throwing exceptions**

> try
> 
> {
> 
> conn.Close();
> 
> }
> 
> catch (InvalidOperationException ex)
> 
> {
> 
> Console.WriteLine(ex.GetType().FullName);
> 
> Console.WriteLine(ex.Message);
> }

- **Design classes so that exceptions can be avoided**

> A class can provide methods or properties that enable you to avoid making a call that would trigger an exception.

- **Throw exceptions instead of returning an error code**

> Exceptions ensure that failures do not go unnoticed because calling code didn\'t check a return code.

- **Use the predefined .NET exception types**
- Throw an InvalidOperationException exception if a property set or
  method call is not appropriate given the object\'s current state.
- Throw an ArgumentException exception or one of the predefined
  classes that derive from ArgumentException if invalid parameters are
  passed.
- **End exception class names with the word Exception**

public class MyFileNotFoundException : Exception

> {
> }

- **Include three constructors in custom exception classes**
- Exception(), which uses default values.
- Exception(String), which accepts a string message.
- Exception(String, Exception), which accepts a string message and an inner exception.
- **Ensure that exception data is available when code executes remotely**

> When you create user-defined exceptions, ensure that the metadata for the exceptions is available to code that is executing remotely.

- **Use grammatically correct error messages**

> Write clear sentences and include ending punctuation. Each sentence in the string assigned to the [Exception.Message](https://docs.microsoft.com/en-us/dotnet/api/system.exception.message#System_Exception_Message) property should end in a period. For example, "The log table has overflowed." would be an appropriate message string.

- **Include a localized string message in every exception**

> The error message that the user sees is derived from the [Exception.Message](https://docs.microsoft.com/en-us/dotnet/api/system.exception.message#System_Exception_Message) property
> of the exception that was thrown, and not from the name of the exception class. Typically, you assign a value to the [Exception.Message](https://docs.microsoft.com/en-us/dotnet/api/system.exception.message#System_Exception_Message) property by passing the message string to the message argument of an [Exception constructor](https://docs.microsoft.com/en-us/dotnet/api/system.exception.-ctor).

- **Place throw statements so that the stack trace will be helpful**

> The stack trace begins at the statement where the exception is thrown and ends at the catch statement that catches the exception.

- **Restore state when methods don't complete due to exceptions**

> Callers should be able to assume that there are no side effects when an exception is thrown from a method. For example, if you have code that transfers money by withdrawing from one account and depositing in another account, and an exception is thrown while executing the deposit, you don't want the withdrawal to remain in effect.

- **Create Your Own C# Custom Exception Types**

> C# exceptions are defined as classes, just like any other C# object. All exceptions inherit from a base System.Exception class. Creating your own C# custom exceptions is really only helpful if you are going to catch that specific type of exception and **handle it
differently**. They can also be helpful to track a very specific type of exception that you deem to extremely critical.Benefits of custom C# Exception types:

- Calling code can do custom handling of the custom exception type
- Ability to do custom monitoring around that custom exception type

> We can handle errors globally with the Built-In Middleware in ASP.NET Core. The UseExceptionHandler middleware is a built-in middleware that we can use to handle exceptions in our [ASP.NET Core Web API](https://code-maze.com/ultimate-aspnet-core-3-web-api/) application. So, let's dive into the code to see this middleware in action. First, we are going to add a new class ErrorDetails in the Models folder:
> 
> using Newtonsoft.Json;
> 
> namespace GlobalErrorHandling.Models
> 
> {
> 
> public class ErrorDetails
> 
> {
> 
> public int StatusCode { get; set; }
> 
> public string Message { get; set; }
> 
> public override string ToString()
> 
> {
> 
> return JsonConvert.SerializeObject(this);
> 
> }
> 
> }
> 
> }
> 
> We are going to use this class for the details of our error message. To continue, let's create a new folder Extensions and a new static class ExceptionMiddlewareExtensions.cs inside it.
> 
> using GlobalErrorHandling.Models;
> 
> using LoggerService;
> 
> using Microsoft.AspNetCore.Builder;
> 
> using Microsoft.AspNetCore.Diagnostics;
> 
> using Microsoft.AspNetCore.Http;
> 
> using System.Net;
> 
> namespace GlobalErrorHandling.Extensions
> 
> {
> 
> public static class ExceptionMiddlewareExtensions
> 
> {
> 
> public static void ConfigureExceptionHandler(this IApplicationBuilder
> app, ILoggerManager logger)
> 
> {
> 
> app.UseExceptionHandler(appError =\>
> 
> {
> 
> appError.Run(async context =\>
> 
> {
> 
> context.Response.StatusCode = (int)HttpStatusCode.InternalServerError;
> 
> context.Response.ContentType = \"application/json\";
> 
> var contextFeature =
> context.Features.Get\<IExceptionHandlerFeature\>();
> 
> if(contextFeature != null)
> 
> {
> 
> logger.LogError(\$\"Something went wrong: {contextFeature.Error}\");
> 
> await context.Response.WriteAsync(new ErrorDetails()
> 
> {
> 
> StatusCode = context.Response.StatusCode,
> 
> Message = \"Internal Server Error.\"
> 
> }.ToString());
> 
> }
> 
> });
> 
> });
> 
> }
> 
> }
> 
> }
> 
> In the code above, we've created an extension method in which we've registered the UseExceptionHandler middleware. Then, we've populated the status code and the content type of our response, logged the error message, and finally returned the response with the custom created object. To be able to use this extension method, let's modify the Configure method inside the Startup class: app.ConfigureExceptionHandler(logger);
> 
> Finally, we can remove the add a **throw new Exception** with a custom message to get the exception, if any, to be handled.

## 4. ES6 and JavaScript Coding Best Practices

### 4.1 Naming Convention and Coding Standard

Below are the JavaScript coding standards, naming conventions, and best practices.

- **Avoid Global variables.**

> Minimize the use of global variables. This includes all data types, objects, and functions. Global variables and functions can be overwritten by other scripts. Use local variables instead.

- **Avoid the use of new Object()**
- Use {} instead of new Object()
- Use \"\" instead of new String()
- Use 0 instead of new Number()
- Use false instead of new Boolean()
- Use \[\] instead of new Array()
- Use /()/ instead of new RegExp()
- Use function (){} instead of new Function()
- **Always declare local variables**

> All variables used in a function should be declared as local variables. Local variables must be declared with the var keyword or the let keyword, otherwise they will become global variables. Strict mode does not allow undeclared variables.

- **Declarations on the top**

It is a good coding practice to put all declarations at the top of each script or function.

This will:

- Give cleaner code
- Provide a single place to look for local variables
- Make it easier to avoid unwanted (implied) global variables
- Reduce the possibility of unwanted re-declarations
- **Initialize variables**

It is a good coding practice to initialize variables when you declare them.

This will:

- Give cleaner code
- Provide a single place to initialize variables
- Avoid undefined values
- **Never declare Number, String or Boolean Objects**

Always treat numbers, strings, or booleans as primitive values. Not as objects.

> Declaring these types as objects, slows down execution speed, and produces nasty side effects:
> 
> var = \"RollsRoyce\";
> var y= new String(\"RollsRoyce\");
> (x === y) // is false because x is a string and y is an object.
> 
> var x= new String(\"RollsRoyce\");
> var y= new String(\"RollsRoyce\");
> (x == y) // is false because you cannot compare objects.

- **Beware of Automatic Type Conversions**

Beware that numbers can accidentally be converted to strings or NaN (Not a Number).

> JavaScript is loosely typed. A variable can contain different data types, and a variable can change its data type:
> 
> var x = \"RollsRoyce\"; // typeof x is a string
> 
> x = 5; // changes typeof x to a number
> 
> When doing mathematical operations, JavaScript can convert numbers to strings:
> 
> var x = 5 + 7; // x.valueOf() is 12, typeof x is a number
> 
> var x = 5 + \"7\"; // x.valueOf() is 57, typeof x is a string

- **Use Parameter Defaults**

> If a function is called with a missing argument, the value of the missing argument is set to undefined.
> 
> Undefined values can break your code. It is a good habit to assign default values to arguments.

- **End the Switches with Defaults**

> Always end your switch statements with a default. Even if you think there is no need for it.

- **avoid == and use ===**

> The == comparison operator always converts (to matching types) before comparison.The === operator forces comparison of values and type:
> 
> 0 == \"\"; // true
> 
> 1 == \"1\"; // true
> 
> 1 == true; // true
> 
> 0 === \"\"; // false
> 
> 1 === \"1\"; // false
> 
> 1 === true; // false

- **avoid the use of eval()**

> The eval() function is used to run text as code. In almost all cases, it should not be necessary to use it. Because it allows arbitrary code to be run, it also represents a security problem.
> 
> Below are the ES6 coding standards and best practices:

- **Strict mode must be used. However, it should be inserted at build time, not in the original source.**
- **Regular objects must be created using the Object syntax literal.**

> // bad
> 
> const obj = new Object();
> 
> const obj = Object.create(Object.prototype);
> 
> // good
> 
> const obj = {};

- **Object literals keys must be camelCase (this doesn\'t apply to programmatically generated keys).**

> // bad
> 
> const obj = {
> 
> \'not-camel-cased\': \...
> 
> };
> 
> // good
> 
> const obj = {
> 
> camelCased: \...
> 
> };

- **An object declaration must have spaces after each { and before each }. If the declaration is multiline, each line must end with a comma, including the last one. If the declaration is not multiline, the last value must not end with a comma. In an object declaration, there must not be space before each colon but at least one after each colon.**

> // bad
> 
> const a = {
> 
> k1: v1,
> 
> k2: v2
> 
> };
> 
> const b = { k1: v1, k2: v2, };
> 
> const c = {k1:v1};
> 
> // good
> 
> const a = {
> 
> k1: v1,
> 
> k2: v2,
> 
> };

- **Arrays must be created using the Array syntax literal.**

> // bad
> 
> const a = new Array();
> 
> // good
> 
> const a = \[\];

- **Static strings must be declared using single quotes or backticks. Dynamic strings must be declared using ES6 template literals (backticks). Dynamic strings must not be declared using single- or double-quotes. Never use double-quotes.**

> // bad
> 
> const a = \"foobar\";
> 
> const b = \'foo\' + a + \'bar\';
> 
> // acceptable
> 
> const c = \`foobar\`;

- **var must not be used. const should be used by default. If you really need to use let, its acceptable, but its most often a sign that you should refactor. const (or let) must be used exactly once per variable declaration. var is to be considered legacy; there are no practical use cases for var anymore. All values (rather than variables) should be const (single-assignment) by default; which means that unless otherwise specified, a value cannot change behind your back.**

> // bad
> 
> const a = 1, b = 2, c = 3;
> 
> // good
> 
> const a = 1;
> 
> const b = 2;
> 
> const c = 3;
> 
> // best
> 
> const \[a, b, c\] = \[1, 2, 3\];

- **Regular (named and hoisted) function declarations should be used instead of anonymous functions by default. new must not be use with functions which are not ES6 classes.**

> // bad
> 
> function A() {
> 
> }
> 
> const a = new A();
> 
> // good
> 
> class A {
> 
> }
> 
> const a = new A();

- **Arrow functions should be used instead of Function.prototype.bind when applicable. self / \_this / that trickery must not be used.**

> function method(\...params) {
> 
> \...
> 
> }
> 
> // terribly bad
> 
> const self = this;
> 
> const boundMethod = function(\...params) {
> 
> return method.apply(self, params);
> 
> }
> 
> // best
> 
> const boundMethod = (\...params) =\> method.apply(this, params);

- **Ternary operator (?:) should be avoided. It must not be used if**
- The whole expression cannot fit on one line;
- The expression involve other ternary operators;
- The members of the expression are too complex to keep it readable.
- **undefined must not be used, void 0 must be used instead.**

> // bad
> 
> if(x === undefined) {
> 
> \...
> 
> }
> 
> // good
> 
> if(x === void 0) {
> 
> \...
> 
> }

- **The order of class methods definitions should always be:**
  
  - constructor
  - public get/set accessors, grouped by name,
  - public methods,
  - private get/set accessors (with a \_ prefix), grouped by name,
  - private methods (with a \_ prefix),
  - public static methods,
  - private static methods (with a \_ prefix).
  - Prototype properties should be defined immediately after the class definition and use Object.assign and should not contain methods (set them in the class definition directly).
- **Promise\#then must not be used with 2 parameters. Promise\#catch must be used instead.Promise\#try should be used for Promise-returning function, instead of return
Promise.resolve/return Promise.reject.**
  
### 4.2 Error Handling

> Handling errors properly is essential in building a robust application in Angular. Error handlers provide an opportunity to present friendly information to the user and collect important data for development. In today\'s age of advanced front-end websites, it\'s more important than ever to have an effective client-side solution for error handling.
> 
> Error Handler class needs to be created to handle the errors coming in the response of the API. By verifying if an error is an instance of ErrorEvent, we can figure out which type of error we have and handle it accordingly.
> 
> ![Error_Handling](../../../images/Coding_Standards_Error.PNG)

## GLOSSARY