# docs

## Typescript


### Interface
```node
interface User {
  id: string;
  name: string;
  email: string;
  password: string;
}
```

### Omit
```node
const newUser: Omit<User, "id"> = {
  name: "John",
  email: "john@doe.com",
  password: "123456",
}
```
### Pick
```node
const newUser: Pick<User, "name" | "email"> = {
  name: "John",
  email: "john@doe.com",
}
```
