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

### Extends
```node
interface User extends PersonInterface {
  id: string;
  name: string;
  email: string;
  password: string;
  // first_name: string; // PersonInterface
  // last_name: string; // PersonInterface
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






### Extends Elements HTML Attributes
#### Interface
```node
interface ButtonProps extends React.ButtonHTMLAttributes<HTMLButtonElement>{
  ...
}
```
#### Type
```node
type ButtonProps = React.ButtonHTMLAttributes<HTMLButtonElement>;
```





### Cast
```node
const users = (await fetch(...)) as User[];
```


### Generics
```node
function identity<T>(arg: T): T {
  return arg; // arg: type T
}
```



