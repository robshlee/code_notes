# SQL Alchemy notes

**output value from query**  
session.query(dbo_events_associate).filter(dbo_events_associate.default_id==associate.id).first().employee_id