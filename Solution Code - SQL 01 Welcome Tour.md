# Solution Code - SQL 01 Welcome Tour

<summary>Step 1 Solution  - Take your first look</summary>
<details>   
```sql
    SELECT * FROM games LIMIT 5;
    
    -- Remember that queries get large very quickly. When that happens
    -- it's common to break them up into multiple lines like this:
    SELECT * 
    FROM games 
    LIMIT 5;
```
</details>

<summary>Step 2 Solution - Focus on one detail</summary>
<details>    
```sql
    SELECT title FROM games LIMIT 10;
    
    -- Optional: Include genre
    SELECT title, genre FROM games LIMIT 10;
```
</details>

<summary>Step 3 Solution - Explore another table</summary>
<details>   
```sql
    SELECT * FROM tournaments LIMIT 5;
```
</details>

<summary>Step 4 Solution - Zoom in with a filter</summary>
<details>    
```sql
    SELECT * FROM tournaments
    WHERE region = 'West'
    LIMIT 5;
    
    -- Optional: filter by status
    SELECT * FROM tournaments
    WHERE status = 'completed'
    LIMIT 5;   
```
</details>

<summary>Step 5 Solution - Look at log data</summary>
<details>    
```sql
    SELECT * FROM error_logs LIMIT 4;
```
</details>

<summary>Step 6 Solution - Spot a filtered result</summary>
<details>    
```sql
    SELECT * FROM error_logs
    WHERE error_type = 'StreamOutage'
    LIMIT 3;
    
    -- Optional: Change the filter
    SELECT * FROM error_logs
    WHERE error_type = 'EncoderError'
    LIMIT 3;
```
</details>

<summary>Step 7 Solution - Explore ticket prices (stretch)</summary>
<details>   
```sql
    -- Sort by most expensive first
    SELECT ticket_id, tournament_id, price_paid
    FROM tickets
    ORDER BY price_paid DESC;
    
    -- Sort by least expensive first
    SELECT ticket_id, tournament_id, price_paid
    FROM tickets
    ORDER BY price_paid ASC;
```
</details>