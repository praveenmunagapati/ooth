# Changelog

## 1.1.1

* Fix next clients (getInitialState).

## 1.1.0

* BREAK: Node 8, react 16, apollo 2 (affecting only packages that were still in 0.X: compose-next, ooth-client-react, ooth-client-react-next, ooth-client-react-next-apollo)

## 1.0.0

* BREAK: Target engine from now on is node 8.

### ooth

* BREAK: Extracted db backend, now need to initialize using `ooth-mongo` (or another backend of your choice).

### ooth-mongo

* Extracted db backend from `ooth` as a standalone package.

### ooth-local

* BREAK: Hash password reset and email validation tokens. They can't be used as keys anymore. To reset a password or validate an email, one has to pass userId parameter as well.
* Password reset and email validation tokens expire after 1 hour.

## 0.7.0

### compose-next

* Handle cases in which parent doesn't have initial props
* transmit original props.

### ooth

* Add support for profileFields. Now only profileFields are exposed on the /status route
* Use `ObjectId` for mysql queries

### ooth-client

* Throw on error

### ooth-local

* Support username
* Support changing password
* Register profile fields