# Liquibase Update To Tag Action
Official GitHub Action to run Liquibase Update To Tag in your GitHub Action Workflow. For more information on how update to tag works visit the [Official Liquibase Documentation](https://docs.liquibase.com/commands/home.html).
## Update To Tag
Deploy changes from the changelog file to the specified tag
## Usage
```yaml
steps:
- uses: actions/checkout@v3
- uses: liquibase-github-actions/update-to-tag@v4.17.0
  with:
    # The root changelog
    # string
    # Required
    changelogFile: ""

    # The tag to update to
    # string
    # Required
    tag: ""

    # The JDBC database connection URL
    # string
    # Required
    url: ""

    # Fully-qualified class which specifies a ChangeExecListener
    # string
    # Optional
    changeExecListenerClass: ""

    # Path to a properties file for the ChangeExecListenerClass
    # string
    # Optional
    changeExecListenerPropertiesFile: ""

    # Changeset contexts to match
    # string
    # Optional
    contexts: ""

    # The default catalog name to use for the database connection
    # string
    # Optional
    defaultCatalogName: ""

    # The default schema name to use for the database connection
    # string
    # Optional
    defaultSchemaName: ""

    # The JDBC driver class
    # string
    # Optional
    driver: ""

    # The JDBC driver properties file
    # string
    # Optional
    driverPropertiesFile: ""

    # Changeset labels to match
    # string
    # Optional
    labelFilter: ""

    # Password to use to connect to the database
    # string
    # Optional
    password: ""

    # Username to use to connect to the database
    # string
    # Optional
    username: ""

```

### Secrets
It is a good practice to protect your database credentials with [GitHub Secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets)

## Optional Liquibase Global Inputs
The liquibase update to tag action accepts all valid liquibase global options as optional parameters. A full list is available in the official [Liquibase Documentation](https://docs.liquibase.com/parameters/command-parameters.html).

### Example
```yaml
steps:
  - uses: actions/checkout@v3
  - uses: liquibase-github-actions/update-to-tag@v4.17.0
    with:
      changelogFile: ""
      tag: ""
      url: ""
      headless: true
      licenseKey: ${{ secrets.LIQUIBASE_LICENSE_KEY }}
      logLevel: INFO
```

## Feedback and Issues
This action is automatically generated. Please submit all feedback and issues with the [generator repository](https://github.com/liquibase/github-action-generator/issues).
