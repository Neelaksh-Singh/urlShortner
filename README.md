# urlShortner
A managed URL shorten-er service, build using Redis and Go Fibre

## 💻 Getting Started

`!!! Having a running Dockerdaemon is a must. !!!` <br>

#### Create a `.env` file *locally* 

Create a `.env` file in the root of your project and insert
key/value pairs as follows:
```sh
DB_ADDR="db:6379"
DB_PASS=""
APP_PORT=":<desired_port>"
DOMAIN="localhost:<desired_port>"
API_QUOTA=<your_desired_limit>
```
`!!! No need to set DB_PASS !!!` <br>

Now once the setup is done, do the following :=>

```console
$ git clone https://github.com/Neelaksh-Singh/urlShortner.git
$ cd urlShortener/
$ docker-compose up -d
```
You are all set to use your very own urlShortner API.

#### Post Request

1. In Postman, make post request to `http://localhost:<your_port>/api/v1`
2. Under Body, Select raw->JSON and then post as follows `{"url":"<url_you_want_to_short>"}`
3. Click Send, and you shall recieve response in JSON format. You will see your shorted URL as well.

### Get Request

1. In Postman, make get request to `http://<your_shorted_url>`
2. Click Send. The API resolves your URL and fetches your website.

