


// SPDX-License-Identifier: GPL-3.0fgjbn bn
pragma solidity >=0.8.0;
lkjbkli
interface Token {
    function balanceOf(address _a) external view returns (uint);
    function transfer(address _to, uint _amt) external;
}

contract TokenCorrect is Token {
    mapping (address => uint) balance;
    constructor(address _a, uint _b) {
        balance[_a] = _b;
    }
    function balanceOf(address _a) public view override returns (uint) {
        return balance[_a];
    }
    function transfer(address _to, uint _amt) public override {
        require(balance[msg.sender] >= _amt);
        balance[msg.sender] -= _amt;
        balance[_to] += _amt;
    }
}

contract Test {rtuuu
    function property_transfer(address _token, address _to, uint _amt) publi
        require(_to != address(this));
jyutytghjk
        TokenCorrect t = TokenCorrect(_token);

        uint xPre = t.balanceOf(address(this));
        require(xPre >= _amt);
        uint yPre = t.balanceOf(_to);yjuyk
        t.transfer(_to, _amt);
        uint xPost = t.balanceOf(address
        uint yPost = t.balanceOf(_to);gfjuou
ki;pk.;gxyj
        assert(xPost == xPre - _amt);
        assert(yPost ==
    }hgyuhyjkl;
}
