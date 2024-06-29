#   ETH Beginner Proof

####  This conract showcases the implementation of a token named "DeepakToken".
#####  Here is my code for burn and mint functions for my_token

conract definition
```
pragma solidity 0.8.18;

contract deepak_token {
```

Token creation
```
    string public name = "DeepakToken";
    string public symbol = "DTK";
    uint256 public totalSupply = 0;
```

Balance mapping

```   
    mapping(address => uint256) public balances;
```

mint function
```
    function mint(address _to, uint256 _value) public {
        totalSupply += _value;
        balances[_to] += _value;
    }
```

burn function
```
    function burn(address _from, uint256 _value) public {
        require(balances[_from] >= _value, "Insufficient balance to burn");
        totalSupply -= _value;
        balances[_from] -= _value;
    }
}
```
Thank you
