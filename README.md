# Project
DECLARE
jenis_kelamin VARCHAR2(30);
tinggi_badan NUMBER(3);

BEGIN
jenis_kelamin := '&jenis_kelamin';
tinggi_badan := &tinggi_badan;

IF ( jenis_kelamin = 'wanita' ) THEN
IF (tinggi_badan >= 160) THEN
DBMS_OUTPUT.PUT_LINE('Selamat WANITA, Anda LULUS seleksi');
ELSIF(tinggi_badan < 160) THEN
DBMS_OUTPUT.PUT_LINE('Mohon Maaf WANITA, Anda TIDAK LULUS seleksi');
END IF;

ELSE
IF(tinggi_badan >=165) THEN
DBMS_OUTPUT.PUT_LINE('Selamat PRIA, Anda LULUS seleksi');
ELSIF(tinggi_badan < 165) THEN
DBMS_OUTPUT.PUT_LINE('Mohon Maaf PRIA, Anda TIDAK LULUS seleksi');
END IF;
END IF;
END;
/
