# Python Queryable Encryption Tutorial

This project demonstrates an example implementation of Queryable Encryption
for the PyMongo driver. To learn more about Queryable Encryption, see the
[Queryable Encryption](https://www.mongodb.com/docs/manual/core/queryable-encryption/quick-start/)
section in the Server manual.

The following sections provide instructions on how to set up and run this project.

## Install Dependencies

To run this sample app, you first need to install the following
dependencies:

- MongoDB Server version 7.0 or later (you can also use [MongoDB Atlas](https://cloud.mongodb.com))
- Automatic Encryption Shared Library version 7.0 or later ([MongoDB Download Center](https://www.mongodb.com/download-center/enterprise/releases))
- `python3`
- `pip`

For more information on installation requirements for Queryable Encryption,
see [Installation Requirements](https://www.mongodb.com/docs/manual/core/queryable-encryption/install/#std-label-qe-install).

## Configure Your Environment

1. Clone this repository

2. Create a file in the root of your directory named `.env`.

3. Copy the contents of `.env.template` into the `.env` file.

4. Replace the placeholder values in the `.env` file with your own credentials.
   For more information on setting credentials, see
   [Quick Start](https://www.mongodb.com/docs/manual/core/queryable-encryption/quick-start/)
   for local key provider credentials.

   > **Tip:** The _SHARED_LIB_PATH_ must point to the actual filename
   > not the folder where it is located
   >> e.g., export SHARED_LIB_PATH=/software/mongo_crypt_shared_v1-macos-arm64-enterprise-7.0.1/lib/mongo_crypt_v1.dylib

5. [Optional] Create a three-node replica set (if you're not using Atlas)

   **Note:** If you are using [mtools](https://github.com/rueckstiess/mtools),
   you can create a replica set by running the following command:

   ```sh
   mlaunch init --replicaset --nodes 3
   ```

## Run the Notebook

1. In a shell, navigate to the directory where you cloned this repo.

2. Create a new Python environment
   ```zsh
   python3 -m venv env
   ```
3. Activate the new Python environment
   ```zsh
   source env/bin/activate
   ```

4. Run `python3 -m pip install -r requirements.txt` to install the Python driver and
   `pymongocrypt`.

5. Run `jupyter lab` to open Jupyter Lab and then open the file _QE.ipynb_.

6. Follow the notebook to insert an encrypted document in MongoDB.

## Notes

The original version of this tutorial is located [here](https://github.com/mongodb/docs/tree/master/source/includes/qe-tutorials/python/)

To install the libmongocrypt on Mac OS:

```sh
brew install mongodb/brew/libmongocrypt
```

Also for Mac OS with M1, the Automatic Encryption Library direct download link is [here](https://downloads.mongodb.com/osx/mongo_crypt_shared_v1-macos-arm64-enterprise-7.0.1.tgz)
