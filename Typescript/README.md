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
### Keyof
```node
type UserProperties = keyof User
```

### Criar tipos através de objetos
```node
const video = {
  title: 'nome do video',
  duration: 120
}

type Video = keyof video;
```

### Omit
```node
const newUser: Omit<User, "id" | "..."> = {
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
### Partial
```node
type UserPartial = Partial<User>

/*
{
  id?: string | undefined;
  name?: string | undefined;
  email?: string | undefined;
  password?: string | undefined;
}
*/
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





### Cast (without checking type)
```node
const users = (await fetch(...)) as User[];
```
### Others
```node
const users: User[] = (await fetch(...));
const users = (await fetch(...)) satisfies User[];
```


### Generics
```node
function identity<T>(arg: T): T {
  return arg; // arg: type T
}
```

### Record
```node
function identity<T extends Record<string, unknown>>(arg: T): T {
  return arg; // arg: type T
}
// T tem que ser um objeto que o nome das propriedades são string e o valor delas qualquer coisa
```




