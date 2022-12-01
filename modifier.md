// SPDX-License-Identifier: GPL-3.0
pragma solidity 0.8.7;

contract Food{

    // Variables
    string public foodItem = "Lasagne";
    address public owner = 0x5B38Da6a701c568545dCfcB03FcB875f56beddC4;
    // Mappings
    // Structs
    // Arrays
    // ENUMs


    // Modifiers
    modifier onlyOwner(){


        
        require(msg.sender == owner,"The account doesnt have access rights");// gate for allowing only valid users
        _;// funcvtion logic
        

    }

    // Functions

    /* function functionName(args) 
                stateMutability 
                visbility 
                modifier *optional
                returns(return datatype){

    }*/
    // Function for adding food
    // stateMutability --> Nothing
    function setFoodItem(string memory _foodItemName)               
                public
                onlyOwner
                {

                    // Require statement
                    //require(condition,"Statement")
        
                    // Function body
                    foodItem =  _foodItemName;
                    
                }

                // msg.sender
                // msg.reciever
                // msg.value

    // Function for reading the data
    // stateMutability --> view
    function getFoodItem()
            view
            public
            onlyOwner
            returns(string memory)
            {

               

                return foodItem;

            }


    // Function for reading food item number
    function getFoodItemOrderNo()
            pure
            public
            returns(uint){

              

                uint _orderNo = 12;// Local variable

                return _orderNo;

            }        


} 
