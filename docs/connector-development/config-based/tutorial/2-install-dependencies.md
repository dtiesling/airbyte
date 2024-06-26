# Step 2: Install dependencies

```bash
cd ../../connectors/source-exchange-rates-tutorial
poetry install
```

These steps create an initial python environment, and install the dependencies required to run an API Source connector.

Let's verify everything works as expected by running the Airbyte `spec` operation:

```bash
poetry run source-exchange-rates-tutorial spec
```

You should see an output similar to the one below:

```
{"type": "SPEC", "spec": {"documentationUrl": "https://docsurl.com", "connectionSpecification": {"$schema": "http://json-schema.org/draft-07/schema#", "title": "Python Http Tutorial Spec", "type": "object", "required": ["TODO"], "additionalProperties": false, "properties": {"TODO: This schema defines the configuration required for the source. This usually involves metadata such as database and/or authentication information.": {"type": "string", "description": "describe me"}}}}}
```

This is a simple sanity check to make sure everything is wired up correctly.
More details on the `spec` operation can be found in [Basic Concepts](https://docs.airbyte.com/connector-development/cdk-python/basic-concepts) and [Defining Stream Schemas](https://docs.airbyte.com/connector-development/cdk-python/schemas).

For now, note that the `main.py` file is a convenience wrapper to help run the connector.
Its invocation format is `python main.py <command> [args]`.
The module's generated `README.md` contains more details on the supported commands.

## Next steps

Next, we'll [connect to the API source](3-connecting-to-the-API-source.md)

## More readings

- [Basic Concepts](https://docs.airbyte.com/connector-development/cdk-python/basic-concepts)
- [Defining Stream Schemas](https://docs.airbyte.com/connector-development/cdk-python/schemas)
- The module's generated `README.md` contains more details on the supported commands.
