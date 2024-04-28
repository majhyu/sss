ewregtrh


// SPDX-License-Identifier: GPL-3.0fgjbn bn
pragma solidity >=0.8.0;vukuyl
lkjbklijhgjm
interface Token {fdvgdddd
    function balanceOf(address _a) external view returns (uint);yuiuiykj
    function transfer(address _to, uint _amt) external;
}h kukjuyyyyyk
tyu57
contract TokenCorrect is Token {
    mapping (address => uint) balance;hyukulu
    constructor(address _a, uint _b) {
        balance[_a] = _b;
    }
    function balanceOf(address _a) public view override returns (uint) {
        return balance[_a];
    }
    function transfer(address _to, uint _amt) public override {
        require(balance[msg.sender] >= _amt);
        balance[msg.sender] -= _amt;
        balance[_to] += _amt;jhgjcivoui
    }
}
iuvvl
contract Test {rtuuurtyukl
    function property_transfer(address _token, address _to, uint _amt) publi
        require(_to != address(this));
jyutytghjk
        TokenCorrect t = TokenCorrect(_token);

        uint xPre = t.balanceOf(address(this));
        require(xPre >= _amt);
        uint yPre = t.balanceOf(_to);yjuyk
        t.transfer(_to, _amt);
        uint xPost = t.balanceOf(address
        uint yPost = t.balanceOf(_to);gfjuoujkgjkjkl
ki;pk.;gxyj
        assert(xPost == xPre - _amt);
        assert(yPost ==ertyhujik
    }hgyuhyjkl;
}
