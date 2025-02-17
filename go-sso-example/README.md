# Go SSO Example
An example Go application demonstrating how to use the [WorkOS Go SDK](https://github.com/workos/workos-go) to authenticate users via SSO.

## Prerequisites
- Go

## Go Project Setup

1. Clone this git repository using your preferred secure method (HTTPS or SSH).
   ```bash
   # HTTPS
   git clone https://github.com/workos/go-example-applications.git
   ```

   or

   ```bash
   # SSH
   git clone git@github.com:workos/go-example-applications.git
   ```

2. Navigate to the cloned repository.
   ```bash
   cd go-example-applications/go-sso-example
   ```

3. Obtain and make note of the following values. In the next step, these will be set as environment variables.
   - Your [WorkOS API key](https://dashboard.workos.com/api-keys)
   - Your [SSO-specific, WorkOS Project ID](https://dashboard.workos.com/configuration)
   - Your [Redirect URI](https://workos.com/docs/sso/guide/set-redirect-uri)


4. Create a new file called ".env" in the root of the project and add the following variables, replacing the xxx with the values from step 4:
   - WORKOS_API_KEY=xxx
   - WORKOS_CLIENT_ID=xxx
   - WORKOS_REDIRECT_URI=xxx
   - WORKOS_CONNECTION=xxx

5. The final setup step is to start the server.
   ```bash
   go run .
   ```

   Navigate to `localhost:8000` in your web browser. You should see a "Login" button. If you click this link, you'll be redirected to an HTTP `404` page because we haven't set up SSO yet!

   You can stop the local server for now by entering `CTRL + c` on the command-line.


## SSO Setup with WorkOS

Follow the [SSO authentication flow instructions](https://workos.com/docs/sso/guide/introduction) to set up an SSO connection.

When you get to the step where you provide the `REDIRECT_URI` value, use [http://localhost:8000/callback].

If you get stuck, please reach out to us at support@workos.com so we can help.

## Testing the Integration

6. Naviagte to the `go-sso-example` directory.

   ```bash
   go run .
   ```

   Once running, navigate to [http://localhost:8000] to test out the SSO workflow.

   Hooray!

## Need help?

If you get stuck and aren't able to resolve the issue by reading our API reference or tutorials, you can reach out to us at support@workos.com and we'll lend a hand.
