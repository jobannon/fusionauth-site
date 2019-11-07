1. The application backend receives the 200 from FusionAuth. The JWT and refresh token from FusionAuth are written back to the browser in HTTP cookies. These cookies are HttpOnly, which prevents JavaScript from accessing them, making them less vulnerable to theft. Additionally, all requests from the browser to the application backend will include these cookies so that the backend can use them. Also, if the application needs the user object, the application backend can send it back in JSON