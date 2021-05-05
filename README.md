# Adding SIM Swap Detection to your Web App's Vonage Verify 2FA Login Flow using **tru.ID** SIMCheck

## Requirements

The requirements for this project are:

- [Node.js](https://nodejs.org)
- A [tru.ID Account](https://tru.id)
- A [Vonage Account](https://developer.nexmo.com/)

## Getting Started

This project uses Vonage's [node-stepup-auth](https://github.com/nexmo-community/node-stepup-auth) as the base in the `starter-files` branch.

Clone the `starter-files` branch via:

```
git clone -b starter-files --single-branch https://github.com/tru-ID/2fa-sim-swap-detection-vonage.git
```

If you're only interested in the finished code in `main` then run:

```
git clone -b main https://github.com/tru-ID/2fa-sim-swap-detection-vonage.git
```

Next you need to configure Vonage using your account credentials.

Copy the values of `example.env` into a `.env` file via:

```
cd 2fa-sim-swap-detection-vonage && cp example.env .env
```

Open the `.env` file and configure the following values:

- `VONAGE_API_KEY`: Your Vonage API key found [on the developer dashboard](https://dashboard.nexmo.com)
- `VONAGE_API_SECRET`: Your Vonage API key found [on the developer dashboard](https://dashboard.nexmo.com)
- `VONAGE_BRAND_NAME`: A name for your application which will appear on the home page and also in the `from` field of any SMS sent via the Verify API. Up to 11 alphanumeric characters

Next, Create a [tru.ID Account](https://tru.id)

Install the **tru.ID** CLI via:

```bash
npm i -g @tru_id/cli

```

Input your **tru.ID** credentials which can be found within the tru.ID [console](https://developer.tru.id/console)

Create a new **tru.ID** project via:

```
tru projects:create sms-2fa-vonage
```

configure the following values in your `.env`:

- `TRU_ID_CLIENT`: The client ID found in the `tru.json` file in the newly created **tru.ID** project.
- `TRU_ID_SECRET`: The client secret found in the `tru.json` file in the newly created **tru.ID** project.

## Restoring Dependencies

In order to restore dependencies run:

```bash
npm install
```

## Starting Project

In order to start the project run:

```bash
npm start
```

## References

- [**tru.ID** docs](https://developer.tru.id/docs)
- [Vonage's node-stepup-auth](https://github.com/nexmo-community/node-stepup-auth)

## Meta

Distributed under the MIT License. See [LICENSE](https://github.com/tru-ID/2fa-sim-swap-detection-vonage/blob/main/LICENSE.md)

[**tru.ID**](https://tru.id)
