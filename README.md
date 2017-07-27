# mobx-form-validator
base on mobx-form-validate

## Installation


## API
#### @validator([{reg,msg},{reg,msg}...])
method fn return regs

## Usage
### example 1
```js
class TestModel {
  @observable
  @validator([
    { required: true,messaeg:'required!' },
    { max: 99, min: 11, message: 'The age range was 11-99 years old' }
  ])
  age
}
```

### example 2
```js
class TestModel {
  max = 99

  min =1

  @observable
  @validator((value,source)=>{
      return [{
           max: source.max, min: source.min, message: 'The age range was 11-99 years old' 
      }]
  })
  age
}
```

## rules

#### type
Ascii
Base64
Boolean
CreditCard
Currency
DataURI
Decimal
Email
Float
HexColor
Hexadecimal
IP
Int
JSON
MACAddress
Numeric
URL
UUID
#### required
#### max
#### min
#### pattern
#### length