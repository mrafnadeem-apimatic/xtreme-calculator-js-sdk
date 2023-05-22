
# Getting Started with APIMATIC Calculator

## Introduction

Simple calculator API hosted on APIMATIC

## Install the Package

Run the following command from your project directory to install the package from npm:

```ts
npm install xtreme-calculator-sdk@1.0.1
```

For additional package details, see the [Npm page for the xtreme-calculator-sdk@1.0.1  npm](https://www.npmjs.com/package/xtreme-calculator-sdk/v/1.0.1).

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/mrafnadeem-apimatic/xtreme-calculator-js-sdk/tree/1.0.1/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| `environment` | Environment | The API environment. <br> **Default: `Environment.Production`** |
| `timeout` | `number` | Timeout for API calls.<br>*Default*: `0` |
| `httpClientOptions` | `Partial<HttpClientOptions>` | Stable configurable http client options. |
| `unstableHttpClientOptions` | `any` | Unstable configurable http client options. |

### HttpClientOptions

| Parameter | Type | Description |
|  --- | --- | --- |
| `timeout` | `number` | Timeout in milliseconds. |
| `httpAgent` | `any` | Custom http agent to be used when performing http requests. |
| `httpsAgent` | `any` | Custom https agent to be used when performing http requests. |
| `retryConfig` | `Partial<RetryConfiguration>` | Configurations to retry requests. |

### RetryConfiguration

| Parameter | Type | Description |
|  --- | --- | --- |
| `maxNumberOfRetries` | `number` | Maximum number of retries. <br> *Default*: `0` |
| `retryOnTimeout` | `boolean` | Whether to retry on request timeout. <br> *Default*: `true` |
| `retryInterval` | `number` | Interval before next retry. Used in calculation of wait time for next request in case of failure. <br> *Default*: `1` |
| `maximumRetryWaitTime` | `number` | Overall wait time for the requests getting retried. <br> *Default*: `0` |
| `backoffFactor` | `number` | Used in calculation of wait time for next request in case of failure. <br> *Default*: `2` |
| `httpStatusCodesToRetry` | `number[]` | Http status codes to retry against. <br> *Default*: `[408, 413, 429, 500, 502, 503, 504, 521, 522, 524]` |
| `httpMethodsToRetry` | `HttpMethod[]` | Http methods to retry against. <br> *Default*: `['GET', 'PUT']` |

The API client can be initialized as follows:

```ts
const client = new Client({
  timeout: 0,
  environment: Environment.Production,
});
```

## List of APIs

* [Simple Calculator](https://www.github.com/mrafnadeem-apimatic/xtreme-calculator-js-sdk/tree/1.0.1/doc/controllers/simple-calculator.md)

## Classes Documentation

* [ApiResponse](https://www.github.com/mrafnadeem-apimatic/xtreme-calculator-js-sdk/tree/1.0.1/doc/api-response.md)
* [ApiError](https://www.github.com/mrafnadeem-apimatic/xtreme-calculator-js-sdk/tree/1.0.1/doc/api-error.md)

