"Change Activity: Process Timesheet Records "

that's bnous bonus

Employee Hours Billed to Project
Full-Time employees
    10335 Finance    Smithers  $110.00/hour 24 hours
    21555 Marketing  Wiggims   $75.00/hour  10 hours
    31004 IT         Burns     $150.00/hour 20 hours
Part-Time employees
   20045 Finance     Flanders  $25.00/hour  10 hours

Print_Hours_Billed_To_Project
Print "Employee Hours Billed to Project" heading
    
    if fulltime
	DOWHILE morerecords exist
	Read timesheet record
        IF timesheet_status = "FT" THEN
            Print EmployeeID, Department, namelast, Billing Rate, Hours Worked
        ENDIF
    ENDDO
    Read timesheet record

else parttime
DOWHILE morerecords exist
	Read timesheet record
        IF timesheet_status = "pT" THEN
            Print EmployeeID, Department, namelast, Billing Rate, Hours Worked
        ENDIF
    ENDDO
END
