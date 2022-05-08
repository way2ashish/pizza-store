# pizza-store
springboot REST based pizza store application


# Example commands to test with Curl
* List all restaurants: `curl -v -H "Content-Type: application/json" -X GET http://localhost:8080/rest/restaurants`
* Add a new restaurant:
  * `curl -v -H "Content-Type: application/json" -X POST -u "admin:admin" -d '{"name":"Amarillo","city":"Tampere","address":"Hatanpäänvaltatie 1","email":"pizza@amarillo.fi","phone":"0207 716 328","open_at":"11:00:00","close_at":"22:00:00"}' http://localhost:8080/rest/restaurant`
  * `curl -v -H "Content-Type: application/json" -X POST -u "admin:admin" -d '{"name":"Rax","city":"Tampere","address":"Hatanpäänvaltatie 1","email":"pizza@rax.fi","phone":"0207 716 328","open_at":"11:00:00","close_at":"22:00:00"}' http://localhost:8080/rest/restaurant` 
  * (without authentication, thus expected to fail) `curl -v -H "Content-Type: application/json" -X POST -d '{"name":"Amarillo","city":"Tampere","address":"Hatanpäänvaltatie 1","email":"pizza@amarillo.fi","phone":"0207 716 328","open_at":"11:00:00","close_at":"22:00:00"}' http://localhost:8080/rest/restaurant` 