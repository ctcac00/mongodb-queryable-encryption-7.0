# Python Queryable Encryption Tutorial

This project demonstrates an example implementation of Queryable Encryption
for the PyMongo driver. To learn more about Queryable Encryption, see the
[Queryable Encryption](https://www.mongodb.com/docs/manual/core/queryable-encryption/quick-start/)
section in the Server manual.

The following sections provide instructions on how to set up and run this project.

## Install Dependencies

To run this sample app, you first need to install the following
dependencies:

- MongoDB Server version 7.0 or later
- Automatic Encryption Shared Library version 7.0 or later
- `python3`
- `pip`

For more information on installation requirements for Queryable Encryption,
see [Installation Requirements](https://www.mongodb.com/docs/manual/core/queryable-encryption/install/#std-label-qe-install).

## Configure Your Environment

1. Create a file in the root of your directory named `.env`.

2. Copy the contents of `.env.template` into the `.env` file.

3. Replace the placeholder values in the `.env` file with your own credentials.
   For more information on setting credentials, see
   [Quick Start](https://www.mongodb.com/docs/manual/core/queryable-encryption/quick-start/)
   for local key provider credentials.

   > **Note:** The sample notebook uses the `pydotenv` package to access
   > the credentials as if they were defined as environment variables, but
   > does not overwrite any environment variables you currently have set.

4. Create a three-node replica set.

   **Note:** If you are using [mtools](https://github.com/rueckstiess/mtools),
   you can create a replica set by running the following command:

   ```sh
   mlaunch init --replicaset --nodes 3
   ```

## Run the Notebook

1. In a shell, navigate to the directory where you cloned this repo.

2. Run `python3 -m pip install -r requirements.txt` to install the Python driver and
   `pymongocrypt`.

3. Run `jupyter lab` to open Jupyter Lab and then open the file _QE.ipynb_.

4. Follow the notebook to insert an encrypted document in MongoDB.

## Notes

The original version of this tutorial is located [here](https://github.com/mongodb/docs/tree/master/source/includes/qe-tutorials/python/)

To install the libmongocrypt on Mac OS:

```sh
brew install mongodb/brew/libmongocrypt
```
