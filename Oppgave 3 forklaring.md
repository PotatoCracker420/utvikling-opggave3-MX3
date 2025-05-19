-- Denne spørringen henter data fra tre tabeller: Bestilling, Bil og Kunde
SELECT 
    bil.*,        -- Henter alle kolonnene fra tabellen 'Bil'
    kunde.*       -- Henter alle kolonnene fra tabellen 'Kunde'
FROM 
    Bestilling    -- Starter med tabellen 'Bestilling'
JOIN 
    Bil ON Bil.id = Bestilling.bil_id       -- Kobler 'Bil' til 'Bestilling' der Bil.id matcher Bestilling.bil_id
JOIN 
    Kunde ON Kunde.id = Bestilling.kunde_id -- Kobler 'Kunde' til 'Bestilling' der Kunde.id matcher Bestilling.kunde_id
;
