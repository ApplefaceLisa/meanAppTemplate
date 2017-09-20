credit to Traversy Media

# Node Authentication API

API for registering users with mongodb and authentication using a JWT (json web token). This app uses passport and passport-jwt and uses a JWT strategy

### Version
1.0.0

## Usage

```bash
npm install
```

```bash
npm start
```

##Endpoints
```bash
POST /users/register
```

```bash
POST /users/authenticate   // Gives back a token
```

```bash
GET /users/profile         // Needs json web token to authorize
```

# how to run
under project root dir,
- open cmd : run `mongod`;
- open another cmd : run `npm start`;
- use postman send GET requirements to `http://localhost:3000` will get index.html;
- use postman send POST to `http://localhost:3000/users/register`, video part3 12:30 :
  - header: key - "Content-Type", value - "application/json";
  - body: raw, {
      "name":"Lisa",
      "email":"lisa@hotmial.com",
      "username":"lisa2017",
      "password":"123456"
    }
    sent and get "user registered".
- use postman send POST to `http://localhost:3000/users/authenticate`, video part4 15:50 :
  - header: key - "Content-Type", value - "application/json";
  - body: raw, {
        "username":"lisa2017",
        "password":"123456"
    }
    sent and get userinfo.

### Reference
- code come from [here](https://github.com/bradtraversy/nodeauthapp)
- tutorial video MEAN Stack Front To Back [part1](https://www.youtube.com/watch?v=uONz0lEWft0), [part2](https://www.youtube.com/watch?v=DQ9pZ2NKXRo&t=64s), [part3](https://www.youtube.com/watch?v=1ZeDy2QI3OE), [part4](https://www.youtube.com/watch?v=6pdFXmTfkeE&t=31s).