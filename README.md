# WholeSale---Management---DBMS
PROJECT SYNOPSIS :
WHOLESALE MANAGEMENT SYSTEM
BY : SHILPA SHAJI MOHAN
MIS : 111903155

PROBLEM STATEMENT :
Wholesale management system to keep track of products, ccustomer details , manufacturers details,
delivery partner details and to view these details and keep track of monetory transactions,delete details .

OBJECTIVE:
    1. Store and manage product details
    2. Store and manage customer , manufacturer and delivery partner details 
    3. Record transaction details
    4. Record payment defaulters 
    5. Check availablity of products 
    6. Customers can check transaction history and order history 

FUNCTIONAL REQUIREMENTS:
       
    1. Add/Update/Delete Products
    2. Add/Update/Delete Manufacturers
    3. Add/Update/Delete Customers
    4. Add/Update/Delete Delivery Partners 
    5. Record current Orders 
    6. Delete Orders
    7. Add transaction Details 
    8. Add Payment details 
    9. Add and manage Shipping Details 
    RELATIONAL SCHEMAS OBTAINED FROM R :


    • PRODUCT  (PID, PNAME,SIZE,UNIT_PRICE,TOT_QTY,MID, CATID)
    • MANUFACTURER  (MID, MNAME, MPHONE)
    • DELIVERY_PARTNER  (DID,DNAME)
    • CUSTOMER  (CID,CNAME,CPHONE,CMAIL)
    • ADDRESS (ID,NAME,BUILDING_NO,STREET_NO,STREET_NAME, CITY,DISTRICT,STATE,COUNTRY,PIN)
    • CATEGORY (CATID,CATNAME)	
    • PAYMENT(ID,PAY_DATE,TOT_AMT,MODE,CID,OID)
    • ORDER(OID,ODATE,P_QTY,DISCOUNT,PID,PNAME,SIZE,UNIT_PRICE, CID)
    • SHIPPING(TRACKID,SHIPDATE,DELIVDATE,DID,OID)
	
FUNCTIONAL DEPENDENCIES:

	PRODUCT :
		PID -> PNAME
		PID -> UNIT_PRICE
		(PID,PNAME,SIZE ) -> TOT_QTY
		(PID,PNAME,SIZE ) -> UNIT_PRIZE
		MID -> PID
		CATID -> PID

	MANUFACTURER :
		MID -> MNAME
		MID -> MPHONE

	DELIVERY_PARTNER:
		DID -> DNAME 

	CATEGORY:
		CATID -> CATNAME 

	CUSTOMER:
		CID-> CNAME 
		CID -> CPHONE
		CID -> CMAIL

	ADDRESS:
		ID -> NAME

	ORDER:
		(OID,ODATE,PID,SIZE) -> DISCOUNT
		(CID) -> OID

	
	PAYMENT:
		(ID ,PAY_DATE) -> TOT_AMT
		(ID ,PAY_DATE) ->  MODE

	SHIPPING:
		TRACKID -> SHIPDATE
		TRACKID -> DELIVDATE
		TRACKID -> OID		
		
