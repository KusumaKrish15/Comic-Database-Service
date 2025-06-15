# Setting up your development environment tutorial
<mark>Adapted from To-do service API: Before you start a tutorial. </mark>

These are the steps you must do before you can run
the tutorials for the **To-Do service**.

Expect this preparation to take about 20 minutes to complete.

## Preparing for the tutorials

The following instructions describe how to prepare for running the tutorials on Windows.
For information about how to prepare MacOS for the tutorials, visit the [MacOS installation guide](macos-installation).

### To complete the tutorials in this section, you need the following:

* A [GitHub account](https://github.com)
* The following software on your development system:
    * [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (for the command line)
    * [GitHub Desktop](https://desktop.github.com) (optional)
    * A fork of the [Comic-Database-Service repo](https://github.com/KusumaKrish15/Comic-Database-Service)
    * A current/LTS version of [node.js](https://nodejs.org/en/)
    * A current version of [json-server](https://www.npmjs.com/package/json-server)
    * A current copy of the database file. You can get this by syncing your fork.
    * The [Postman desktop app](https://www.postman.com/downloads/). Because you run the **Comic Database Service** on your development system with an `http://localhost` hostname, the web-version of Postman can't perform the exercises.

## Test your development system

To test your development system, follow these steps:

1. Create and checkout a test branch of your fork of the comic-database-service repo. Your `GitHub repo workspace` is the directory that contains your fork of the `comic-database-service` repo.

    ```shell
    cd <your GitHub repo workspace>
    ls
    # (see the to-do-service directory in the list)
    cd to-do-service
    git checkout -b tutorial-test
    cd api
    json-server -w to-do-db-source.json
    ```

    If your development system is installed correctly, you should see
    the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

    ```shell
    curl http://localhost:3000/users
    ```

3. If the service is running correctly, you should see a list of users from the service, such as in this example.

    ```js
    [
        {
            "last_name": "Smith",
            "first_name": "Ferdinand",
            "email": "f.smith@example.com",
            "id": 1
        },
        {
            "last_name": "Jones",
            "first_name": "Jill",
            "email": "j.jones@example.com",
            "id": 2
        },
        ...
    ```

If you don't see the list of users, or receive an error in any step
of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of users from the service, you're ready to do
the tutorials.
