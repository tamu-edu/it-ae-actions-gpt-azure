# it-ae-actions-gpt-azure

GitHub Composite Action for generating responses via ChatGPT.

## Prequisites
This Action uses OIDC authentication via Azure, so ensure that you have:

1. Created a Service Principal and OIDC federation to GitHub
2. Assigned the `Coginitive Services User` role

Details on how to handle the OIDC federation [can be found here](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-azure)

## Inputs
This composite Action supports a number of ChatGPT parameters, all of which can
be found by looking at the [compose workflow file](action.yaml).

The inputs required to make the Action work are the following:

1. api-base-url
2. azure-client-id
3. azure-subscription-id
4. gpt-model-deployment-name
5. prompt

The last input, `prompt`, is the GPT prompt text that is used to generate a response