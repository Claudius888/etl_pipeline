# Data engineering project: data extraction to analysis
# Architecture diagram

![Architecture](/assets/images/arch.png)
# Running the project

## Prerequisites

1. [Docker](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install/) v1.27.0
2. [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Spin up

In your project directory run the following command.

```bash
make up
docker ps # to see all the components
```

Wait for about a minute. You can log into

1. Dagster UI at [http://localhost:3000/](http://localhost:3000/)
2. Metabase UI at [http://localhost:3001/](http://localhost:3001/). Use the following credentials

```bash
username: joshua.joseph@psg.fr
password: password1234
```

Make sure to switch on the data pipeline in dagster UI, and let it run a few times. In Metabase UI, search for and click on `Online store overview` using the search bar on the top left corner. This will take you to the dashboard which is fed with the transformed data from the data pipeline.

## Tear down

When you are done, you can spin down your containers using the following command.

```bash
make down
```