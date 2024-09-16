### Key: Target
```w00: https://go.w00.io```
### Options
#### Delay before redirecting
```- delay:3```
#### Additional aliases (keys) to handle
```- alias:a,b,c```
#### HTML to show before redirecting
- $0 -> Key
- $1 -> Target

```- prehtml: "<h2>Redirecting from $0 to $1</h2>"```
#### Modify CSS for ```prehtml```
```- css prehtml: "CSS"```
#### Modify CSS for ```require continue button```
```- css button: "CSS"```
#### How to handle redirects
- ```true```     - disables automated delay + add button
- ```false```    - disables automated delay + add button disabled
- ```disabled``` - remove button

```- require continue button: true```
#### Do not inherit a global setting
disables the prehtml global setting for this key  
```- disable: prehtml```
### Default handler for unmatched keys
Can receive all options like other keys  
```default: https://www.google.com```
### Default options which will be inherited to keys, unless disabled with ```disable``` or configured for a key
```
global:
- delay:3
- prehtml: "<h2>Redirecting from $0 to $1</h2>"
- require continue button: true
```
### Sample
```yaml
w00: https://go.w00.io
- delay:3
- alias:a,b,c
- prehtml: "<h2>Redirecting from $0 to $1</h2>"
- require continue button: true
woo: https://go.w00.io
zto: https://zto.one
- disable: prehtml
default: https://www.google.com
global:
- delay:3
- prehtml: "<h2>Redirecting from $0 to $1</h2>"
- require continue button: true```
