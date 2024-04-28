# Medusa IntegrAI

This is a Proof of Concept version of MedusaJS Integration platform built upon **LLama3 LLM model**. It can integrate MedusaJS with literally anything which could be accesed via TypeScript code. No coding skill required.

LLM aspect is pretty import in this project because all Import and Export operations are **generated by AI**. You only need to prompt the description of your data input our output and we'll do the rest - generating the suitable importer or exporter code that you can run anytime.

No ChatGPT API Key required - because all the models run locally on your PC. It's working pretty well even on CPU-only Macbook (2018), however GPU is recommended.

## Installation

To install the required dependencies, run the following command:

```
docker-compose up
```

It may take a while because this command is downloading the latest LLama3 distribution (4.7GB). Then it's also installing MedusaJS, Postgres DB and so on.

## Usage

To run the application in development mode, use the following command:

```
docker-compose run npm run dev
```

This command uses `nodemon` and `tsx` to automatically restart the application whenever changes are made to the source files.

## Ollama Web-UI

There's a Ollama WebUI instance defined in the default `docker-compose` file and after all is up - it should be available on `http://localhost:8080`

## Medusa JS instance

There's also a Medusa test instance defined in the `docker-compose` file - which is by default run on `http://localhost:9000/app/login`

To add a default admin user please run:

```
docker-compose run medusa npx medusa user -e some@email.com -p some-password 
```

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
```
