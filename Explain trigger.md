CREATE DATABASE library_db;
USE library_db;

CREATE TABLE book_det (
bid INT PRIMARY KEY,
btitle VARCHAR(100),
copies INT
);

CREATE TABLE book_issue (
bid INT,
sid INT,
btitle VARCHAR(100)
);

DELIMITER //

CREATE TRIGGER book_copies_deducts
AFTER INSERT ON book_issue
FOR EACH ROW
BEGIN
UPDATE book_det
SET copies = copies - 1
WHERE bid = NEW.bid;
END//

DELIMITER ;

INSERT INTO book_det (bid,btitle,copies) VALUES
(101,'Wings of Fire',3),
(102,'Harry Potter',5);

SELECT * FROM book_det;

INSERT INTO book_issue (bid,sid,btitle) VALUES
(101,1,'Wings of Fire');

SELECT * FROM book_det;
