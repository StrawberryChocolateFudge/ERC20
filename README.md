## ERC20

This is a generic ERC20 contract based on the OpenZeppelin library.

## Constructor

    constructor(
    	string memory name_,
    	string memory symbol_,
    	uint256 initialSupply
    )

To deploy this function, pass in the name, the symbol and the initial supply of the token. The initial supply will be allocated to the creator's address

## View Functions

    function name() public view virtual override returns (string memory);

Returns the name of the token

    function symbol() public view virtual override returns (string memory)

Returns the symbol of the token

    function decimals() public view virtual override returns (uint8);

Returns the decimals of the token, it's always 18.

    function totalSupply() public view virtual override returns (uint256);

Returns the total supply of the token.

     function balanceOf(address account)
        public
        view
        virtual
        override
        returns (uint256);

Fetch the balance of an account with this.

    function allowance(address owner, address spender)
    	public
    	view
    	virtual
    	override
    	returns (uint256)

Get the approved allowance of a spender granted by the owner.

## State Change

    function transfer(address to, uint256 amount)
    	public
    	virtual
    	override
    	returns (bool);

Transfer tokens to an address.

    function approve(address spender, uint256 amount)
    	public
    	virtual
    	override
    	returns (bool);

Approve the spender address to spend from your balance.

    function transferFrom(
    	address from,
    	address to,
    	uint256 amount
    ) public virtual override returns (bool);

Transfer the approved spend from a balance to another.

    function increaseAllowance(address spender, uint256 addedValue)
    	public
    	virtual
    	returns (bool);

Increase the allowance of the spender

    function decreaseAllowance(address spender uint256 subtractedValue)
    	public
    	virtual
    	returns (bool)

Decrease the allowance of the spender
