# ansible-grp

Install and configure Kaznet web app.

## How it works

This role depends on the [ansible-django](https://github.com/onaio/ansible-django) and [ansible-react](https://github.com/onaio/ansible-react) roles.

Basically, this is what it does:

1. Installs the GRP frontend React application and builds it
2. Installs Redis
3. Installs the GRP web server, which is a Django application
4. Copies the files that result from the React build in step 1 into the Django static files directory
5. Finishes setting up Django
6. Installs SSL certificates if necessary

## Role variables

You can see all variables by looking at the `defaults/main.yml` file.

You can look at `tests/test.yml` for examples of how to use these variables.

## Testing

This project comes with a Vagrantfile, this is a fast and easy way to test changes to the role, fire it up with `vagrant up`.

See [vagrant docs](https://docs.vagrantup.com/v2/) for getting setup with vagrant

## License

Apache 2

## Authors

[Ona Engineering](https://ona.io)
