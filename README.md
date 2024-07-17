# NFT Token (ERC721) Factory

Factory Blockchain Pattern to create Non-Fungible Token (NFTs) utilizing ERC-721 Standards.

![Logo](https://alexandrebarros.com/global/nft-token-factory.png)

## Token

- It is a Basic asset transfer control.

## Factory

- Generate a new smart contract
- Often used for generating new token contracts

## Identicon

An Identicon is a visual representation of a hash value, usually of an IP address, that serves to identify a user of a computer system as a form of avatar while protecting the user's privacy. The original Identicon was a 9-block graphic, and the representation has been extended to other graphic forms by third parties.

## Screen Shot
![Logo](http://alexandrebarros.com/global/TokenFactory_ScreenShot.png)

## Example

```js
contract CarFleet {
  address[] fleet;
  function createChildContract(string make, string model) public payable {
    address newCar = new Car(make, model);
    fleet.push(newCar);
  }
  function getDeployedChildContracts() public view returns (address[]) {
    return fleet;
  }
}
contract Car {
  string public make;
  string public model;
  function Car(string _make, string _model) public {
    make = _make;
    model = _model;
  }
}
```

## Run the tests with Truffle

```bash
truffle console
compile
migrate --reset
test
```
