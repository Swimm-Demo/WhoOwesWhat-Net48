---
title: Tests Overview
---
# Test Files Structure

```
WhoOwesWhat.Tests/
│
├── TestPersonQuery.cs
├── packages.config
├── WhoOwesWhat.Tests.csproj
├── app.config
├── WhoOwesWhat.Tests.csproj.DotSettings
├── TestPostQuery.cs
├── UserTestsNunit.cs
├── TestGroupQuery.cs
├── TestPersonQuery - Copy.cs
│
├── Service.Controller/
│   ├── UserControllerGetPersonTests.cs
│   ├── SyncControllerTest_SyncOfflineFriend.cs
│   ├── FriendrequestControllerSendFriendRequestTests.cs
│   ├── UserControllerAuthenticationTests.cs
│   ├── FriendrequestControllerGetFriendRequestTests.cs
│   ├── FriendrequestControllerAcceptFriendrequestTests.cs
│   ├── SyncControllerTest_SyncToApp.cs
│   ├── SyncControllerTest_SyncPost.cs
│
├── Properties/
│   ├── AssemblyInfo.cs
│
├── DataProvider/
│   ├── UserCredentialDataproviderSaveUserTests.cs
│   ├── UserCredentialDataproviderLogicTests.cs
│   ├── UserCredentialDataproviderTests.cs
│   ├── UserDataProviderFixieTests.cs
│   ├── UserCredentialDataproviderGetUserCredentialsTests.cs
│   │
│   ├── PostTests/
│   │   ├── PostDataproviderLogicTests.cs
│   │   ├── Command/
│   │   │   ├── SavePostTests.cs
│   │
│   ├── PersonTests/
│   │   ├── PersonDataproviderLogicTests.cs
│   │   ├── Command/
│   │   │   ├── SavePersonTests.cs
│   │   ├── Query/
│   │   │   ├── GetPersonTests.cs
│   │   │   ├── PersonQueryTests.cs
│   │
│   ├── FriendTests/
│       ├── Query/
│       │   ├── GetFriendsTests.cs
│
├── Domain/
│   ├── FriendrequestRepository/
│   │   ├── AcceptFriendrequestTests.cs
│   │   ├── SendFriendrequestTests.cs
│   │   ├── GetFriendrequestsTests.cs
│   │
│   ├── FriendRepository/
│   │   ├── SyncOnlineFriendTests.cs
│   │   ├── GetFriendsToAppTests.cs
│   │   ├── DeleteOfflineFriendLogicTests.cs
│   │   ├── SyncOfflineFriendTests.cs
│   │
│   ├── UserRepository/
│   │   ├── UserRepositoryLogicTests.cs
│   │   ├── CreateUserTests.cs
│   │   ├── AuthenticateUserTests.cs
│   │
│   ├── PostRepository/
        ├── SyncPostsTests.cs
        ├── SyncPostsQueryTests.cs
```

# Testing Frameworks, Strategies and Libraries

## Frameworks

### <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="7:2:2" line-data="using NUnit.Framework;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`NUnit`</SwmToken>

<SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="7:2:2" line-data="using NUnit.Framework;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`NUnit`</SwmToken> is a unit-testing framework for all .NET languages. It supports a broad range of .NET platforms, including .NET Core and .NET Framework. <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="7:2:2" line-data="using NUnit.Framework;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`NUnit`</SwmToken> provides a console runner, which can be used by developers to run tests, and it is also compatible with a number of third-party test runners, including those provided with Visual Studio and ReSharper.

<SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="7:2:2" line-data="using NUnit.Framework;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`NUnit`</SwmToken> uses attributes to identify tests and control how they are run. For example, the <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="42:1:3" line-data="        [Test]" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`[Test]`</SwmToken> attribute indicates a method is a test method, and the <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="29:1:3" line-data="        [SetUp]" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`[SetUp]`</SwmToken> attribute is used to denote a method that is called before each test method in a test class.

<SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="7:2:2" line-data="using NUnit.Framework;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`NUnit`</SwmToken> supports a wide variety of assertions, which are static methods of the `Assert` class. These include equality, identity, comparison, type-related, boolean, null, and collection-related assertions.

#### Strategy

Unit Testing

#### Usage

The tests use the <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="7:2:2" line-data="using NUnit.Framework;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`NUnit`</SwmToken> framework with the Moq library for mocking dependencies. Each test is annotated with \[Test\], and setup code is annotated with <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="29:1:3" line-data="        [SetUp]" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`[SetUp]`</SwmToken>. The tests follow a given-when-then structure, where the initial state is set up, an action is performed, and the outcome is verified.

#### Examples

<SwmSnippet path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" line="29" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v">

---

**<SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="29:2:2" line-data="        [SetUp]" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`SetUp`</SwmToken> Method**

The <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="29:2:2" line-data="        [SetUp]" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`SetUp`</SwmToken> method initializes the test environment before each test runs. It resets the kernel and sets up a default owner person object.

```c#
        [SetUp]
        public void SetUp()
        {
            _kernel.Reset();

            _ownerPerson = new Person()
            {
                PersonGuid = new Guid("FAD0CC47-1337-1337-1337-0B34360C33FA"),
                Displayname = "Garg1337",
                IsDeleted = false
            };
        }
```

---

</SwmSnippet>

<SwmSnippet path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" line="42" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v">

---

**<SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="43:5:5" line-data="        public void When_sending_a_friendrequest__it_should_succeed()" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`When_sending_a_friendrequest__it_should_succeed`</SwmToken>**

This test verifies that sending a friend request succeeds when the conditions are met. It mocks the necessary dependencies and verifies that the friend request is saved correctly.

```c#
        [Test]
        public void When_sending_a_friendrequest__it_should_succeed()
        {
            /*
             
                Action: Send friendrequest

                Before:
                Geir legger til Marianne og Beate som Online friends
                Geir sender friendrequest til Victor
                
                After:
                Ny friendrequest mellom Geir og Victor blir lagret

            */

            var friendMarianne = new Person()
            {
                PersonGuid = new Guid("14DD5F5A-4747-4747-4747-64A821B1EAA0"),
                Displayname = "Marianne",
                IsDeleted = false
```

---

</SwmSnippet>

<SwmSnippet path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" line="109" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v">

---

**<SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="110:5:5" line-data="        public void When_sending_a_friendrequest__it_should_fail()" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`When_sending_a_friendrequest__it_should_fail`</SwmToken>**

This test checks that sending a friend request fails if the friend is already in the friend list. It ensures that no new friend request is saved in this scenario.

```c#
        [Test]
        public void When_sending_a_friendrequest__it_should_fail()
        {

            // Fail because the friend is already a Friend

            var friendMarianne = new Person()
            {
                PersonGuid = new Guid("14DD5F5A-4747-4747-4747-64A821B1EAA0"),
                Displayname = "Marianne",
                IsDeleted = false
            };

            var friendBeate = new Person()
            {
                PersonGuid = new Guid("651FEC7D-1C43-4099-AF11-A8E59EA2BAE5"),
                Displayname = "Beate",
                IsDeleted = false
            };

            const string username = "smurf@smurf.com";
```

---

</SwmSnippet>

<SwmSnippet path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" line="161" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v">

---

**<SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="162:5:5" line-data="        public void When_sending_a_friendrequest__it_should_fail2()" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`When_sending_a_friendrequest__it_should_fail2`</SwmToken>**

This test ensures that sending a friend request to oneself fails. It verifies that no friend request is saved and an exception is thrown.

```c#
        [Test]
        public void When_sending_a_friendrequest__it_should_fail2()
        {

            // Fail because you cannot befriend yourself

            var friendMarianne = new Person()
            {
                PersonGuid = new Guid("14DD5F5A-4747-4747-4747-64A821B1EAA0"),
                Displayname = "Marianne",
                IsDeleted = false
            };

            var friendBeate = new Person()
            {
                PersonGuid = new Guid("651FEC7D-1C43-4099-AF11-A8E59EA2BAE5"),
                Displayname = "Beate",
                IsDeleted = false
            };

            const string username = "smurf@smurf.com";
```

---

</SwmSnippet>

<SwmSnippet path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" line="213" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v">

---

**<SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="214:5:5" line-data="        public void When_sending_a_friendrequest__it_should_fail3()" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`When_sending_a_friendrequest__it_should_fail3`</SwmToken>**

This test verifies that sending a duplicate friend request fails if a request has already been sent to the same person. It checks that no new friend request is saved and an exception is thrown.

```c#
        [Test]
        public void When_sending_a_friendrequest__it_should_fail3()
        {

            // Fail because you already have sent a friendrequest to that peson

            var friendMarianne = new Person()
            {
                PersonGuid = new Guid("14DD5F5A-4747-4747-4747-64A821B1EAA0"),
                Displayname = "Marianne",
                IsDeleted = false
            };

            var friendBeate = new Person()
            {
                PersonGuid = new Guid("651FEC7D-1C43-4099-AF11-A8E59EA2BAE5"),
                Displayname = "Beate",
                IsDeleted = false
            };

            const string username = "smurf@smurf.com";
```

---

</SwmSnippet>

<SwmSnippet path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" line="269" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v">

---

**<SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="270:5:5" line-data="        public void When_sending_a_friendrequest__it_should_succeed2()" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`When_sending_a_friendrequest__it_should_succeed2`</SwmToken>**

This test checks that sending a friend request succeeds when there is already a pending friend request from the other person. It ensures that the friend request is automatically accepted.

```c#
        [Test]
        public void When_sending_a_friendrequest__it_should_succeed2()
        {
            /*
             
                Action: Send friendrequest

                Before:
                Geir logger inn på mobil(id:1)
                Marianne logger inn på mobil(id:2)
                Geir sender friendrequest til Marianne
                Marianne sender friendrequest til Geir
                
                After:
                Automatisk lag nye Friends fordi det finnes allerede en Friendrequest fra Geir

            */

            var friendMarianne = new Person()
            {
                PersonGuid = new Guid("14DD5F5A-4747-4747-4747-64A821B1EAA0"),
```

---

</SwmSnippet>

<SwmSnippet path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" line="337" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v">

---

**<SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="338:5:5" line-data="        public void When_sending_a_friendrequest__it_should_succeed3()" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`When_sending_a_friendrequest__it_should_succeed3`</SwmToken>**

This test verifies that sending a new friend request is allowed after a previous request was deleted. It ensures that the new friend request is processed correctly.

```c#
        [Test]
        public void When_sending_a_friendrequest__it_should_succeed3()
        {
            /*
                Action: Send friendrequest

                Before:
                Geir logger inn på mobil(id:1)
                Marianne logger inn på mobil(id:2)
                Geir sender friendrequest til Marianne
                Marianne accepts friendrequest
                Geir sletter friendrequest til Marianne, og synkroniserer
                Marianne synkroniserer
                Geir sender nytt Friendrequest til Marianne
                
                After:
                Det er lov til å sende nytt Friendrequest. Marianne får da ny mulighet til å bli venn med Geir.
            */

            var friendMarianne = new Person()
            {
```

---

</SwmSnippet>

## Libraries

### <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="3:2:2" line-data="using FluentAssertions;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`FluentAssertions`</SwmToken>

This is a .NET library that provides a more readable, fluent way to write assertions in your tests. It extends the basic assertion methods of .NET test frameworks like <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="7:2:2" line-data="using NUnit.Framework;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`NUnit`</SwmToken> and xUnit.

### <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="4:2:2" line-data="using Moq;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`Moq`</SwmToken>

This is a popular mocking framework for .NET. It's used in unit testing to isolate the system under test from its dependencies.

### <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="5:2:2" line-data="using Ninject;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`Ninject`</SwmToken>

This is a lightweight dependency injection framework for .NET. It's used to manage dependencies between classes, which is especially useful in testing when you want to substitute real dependencies with mock objects.

### <SwmToken path="/WhoOwesWhat.Tests/Domain/FriendrequestRepository/SendFriendrequestTests.cs" pos="6:2:6" line-data="using Ninject.MockingKernel.Moq;" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48">`Ninject.MockingKernel.Moq`</SwmToken>

This is an extension for Ninject that integrates it with Moq, allowing you to automatically create mock objects for your dependencies when using Ninject to resolve your classes.

*This is an auto-generated document by Swimm AI 🌊 and has not yet been verified by a human*

<SwmMeta version="3.0.0"><sup>Powered by [Swimm](https://app.swimm.io/)</sup></SwmMeta>
