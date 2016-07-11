SELECT hacker_id, 
       NAME 
FROM   (SELECT s.hacker_id, 
               h.NAME, 
               Count(1) cnt 
        FROM   submissions s 
               INNER JOIN hackers h 
                       ON s.hacker_id = h.hacker_id 
               INNER JOIN challenges c 
                       ON s.challenge_id = c.challenge_id 
               INNER JOIN difficulty d 
                       ON c.difficulty_level = d.difficulty_level 
                          AND s.score = d.score 
        GROUP  BY s.hacker_id, 
                  h.NAME)a 
WHERE  cnt > 1 
ORDER  BY cnt DESC, 
          hacker_id; 
