pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public name = "MyToken";
    string public symbol = "MTK";
    uint256 public totalSupply = 0;

    // mapping variable here
    mapping(address => uint256) public balances;

    // mint function
    function mint(address _to, uint256 _value) public {
        totalSupply += _value;
        balances[_to] += _value;
    }

    // burn function
    function burn(address _from, uint256 _value) public {
        require(balances[_from] >= _value, "Insufficient balance to burn");
        totalSupply -= _value;
        balances[_from] -= _value;
    }
}# begineer_Etherum_project
