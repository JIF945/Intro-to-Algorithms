## Selection Operation 
    The selection operation takes rows from one table and creates a new table

    SELECT * from patient
    WHERE patientID = 223344
    
    The SELECT statement identifies the records that are being requested , and the asterisk means everthing from that table. the prameter after FROM identifies the table name (Patient). the next keyword WHERE, is the condition the query requesting. 
![alt text](/Scripting%20&%20Programming%20Foundations/SQL/Notes/SelectOperation.png "screenshot")
    

## Union Operations
    The Union operation combines distinct distant fields from multiple tables that have the same set of attributes and data types

    SELECT PatientID, LastName FROM patient
    UNION
    SELECT NurseID, LastName FROM Nurse;
![alt text](/Scripting%20&%20Programming%20Foundations/SQL/Notes/UnionOperation.png "screemshot")

## Product Operation 
    The product operation created a result table that includes all of the attributes from the two tables; each row of the second table is added to each row of the first table
    SELECT shifts WingSegment, Shifts.Shift, NurseName.LastName
    FROM shifts
    CROSS JOIN NurseName;
![alt text](/Scripting%20&%20Programming%20Foundations/SQL/Notes/ProductOperation.png "Screenshot")

## Joint Operation 
    A join operation combines two tables, but records are only appended when a matching criterion is met. the results table includes a row with attributes of both tables only when arrributes from the database table match rlated attributes from the second database table
    SELECT *
    FROM patient, Nurse;
    This Syntax selects all the fields from both patient and Nurse tables and joins them into on large table. the is refrerred to as an implicit join. alternatively, to get the same results, an explicit join can be used as shown below.
    SELECT *
    FROM Patient CROSS JOIN Nurse;
![alt text](/Scripting%20&%20Programming%20Foundations/SQL/Notes/JoinOperation.png "screenshot")





