// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.0;// Any version greater than 0.8.0

contract Holidays{

    // Variables
    string[] public destinations;
    //["Barbados","Prague","Antartica","Maldives","Amsterdam","Japan","peoples republic of korea","Thailand","rio de janeiro "];

    // Zero indexing in arrarys.
    // Function for accessing any element
    function getDestinations(uint _listItem) public view returns (string memory) {
        return destinations[_listItem];
    }

    // Challenge is to add the destinations dynamically
    // For dynamic arrays to add new data
    // array.push(item)

    function setDestinations(string memory _destination) public{

        destinations.push(_destination);

    } 

} 
