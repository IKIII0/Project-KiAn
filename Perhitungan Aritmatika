program ProjectKiAn;
uses crt;

type aritmatika = record
    suku_ke: integer;
    suku_awal:real;
    pola_suku:real;
    end;

var 
    nilai: array[1..99] of aritmatika ; //menginisialisai nilai ke record dan array sampai 99 (untuk waspada aja)
    pilih,pilih_mana, n:integer;
    hasil:real;
    ulang:char;

label
    keluar;
    
//===============================================================
//=====================FUNCTION PANGKAT==========================
function pangkat(angkanya:real; pangkatnya:integer):real;
var 
    i:integer;
    hacil:real;
begin
    hacil:= 1; 
    for i := 1 to pangkatnya do  //perulangan untuk menghitung pangkat
        hacil := hacil * angkanya;
    pangkat:= hacil; //mengembalikan nilai ke pangkat untuk parameter keluaran
end;
//===============================================================
//=====================FUNCTION ARITMATIKA=======================
function baris_aritmatika(n, a, b: real):real;
begin
    baris_aritmatika := a + (n - 1) * b; //rumus baris aritmatika
end;

function deret_aritmatika(n, a, b: real):real;
begin
    deret_aritmatika := (n / 2) * (2 * a + (n - 1) * b); //rumus deret aritmatika
end;
//===============================================================
//=====================FUNCTION GEOMETRI=========================
function deret_geometri(n, a, r: real):real;
begin
    if r = 1 then
        deret_geometri := a * n
    else
        deret_geometri := a * (1 - pangkat(r, trunc(n))) / (1 - r); //rumus deret geometri
end;

function baris_geometri(n, a, r: real):real;
begin
    baris_geometri := a * pangkat(r, trunc(n-1)); //rumus baris geometri
end;
//===============================================================
//=====================PROCEDURE TABEL===========================
procedure tabel;
begin
    gotoxy(45,2);write('==========================================================');
    gotoxy(45,3);write('==                     \\((HASIL))//                    ==');
    gotoxy(45,4);write('==========================================================');
    gotoxy(45,5);write('==                                                      ==');
    gotoxy(45,6);write('==                                                      ==');
    gotoxy(45,7);write('==                                                      ==');
    gotoxy(45,8);write('==========================================================');
end;
//===============================================================
//===============================================================
//=====================PROGRAM UTAMA=============================
begin 
    keluar:
    repeat
    clrscr;
    writeln('1.Aritmatika');
    writeln('2.Geometri');
    writeln('3.Keluar');
    write('Silahkan Pilih : ');readln(pilih_mana); //Mau pilih yang aritmatika atau geometri

//====================================================================================================
    if pilih_mana = 1 then
        begin
            clrscr;
            writeln('1.Deret Aritmatika');
            writeln('2.Baris Aritmatika');
            writeln('3.Kembali');
            write('Silahkan Pilih Mau Perhitungan Apa: ');readln(pilih); //mau pilih aritmatika yang mana
//==============================PROGRAM UTAMA DERET ARITMATIKA=========================================
            if pilih = 1 then
            begin
                writeln;
                writeln('=====DERET ARITMATIKA=====');
                write('Masukan mau suku ke berapa (n): '); readln(nilai[1].suku_ke);
                write('Masukan Suku awal          (a): '); readln(nilai[1].suku_awal);
                write('Masukan Pola nya           (b): '); readln(nilai[1].pola_suku);
                hasil:=deret_aritmatika(nilai[1].suku_ke,nilai[1].suku_awal,nilai[1].pola_suku); //masuk ke function sekaligus mengisialisasi nilainya
                writeln;
            tabel;
            gotoxy(60,6);writeln('Suku ke-',nilai[1].suku_ke,' dengan nilai: ',hasil:0:2); //ini hasilnya
            end
//=====================================================================================================
//==============================PROGRAM UTAMA BARIS ARITMATIKA=========================================
            else if pilih = 2 then 
            begin
                writeln;
                writeln('=====BARIS ARITMATIKA=====');
                write('Masukan mau suku ke berapa (n): '); readln(nilai[2].suku_ke);
                write('Masukan Suku awal          (a): '); readln(nilai[2].suku_awal);
                write('Masukan Pola nya           (b): '); readln(nilai[2].pola_suku);
                hasil:=baris_aritmatika(nilai[2].suku_ke,nilai[2].suku_awal,nilai[2].pola_suku); //masuk ke function sekaligus mengisialisasi nilainya
                writeln;
                tabel;
                gotoxy(60,6);writeln('Suku ke-',nilai[2].suku_ke,' dengan nilai ',hasil:0:2); //ini hasilnya
            end
//====================================================================================================
            else if pilih = 3 then
            begin
                goto keluar; //kembali ke program utama
            end
            else
            begin
                exit; //kalau gak milih kembali program nya berhenti
            end
        end
//====================================================================================================
    else if pilih_mana = 2 then 
        begin
            clrscr;
            writeln('1.Deret Geometri');
            writeln('2.Baris Geometri');
            writeln('3.Kembali');
            write('Silahkan Pilih Mau Perhitungan Apa: ');readln(pilih); //mau pilih geometri yang mana
//====================================================================================================
//==============================PROGRAM UTAMA DERET GEOMETRI==========================================
            if pilih = 1 then
            begin
                writeln;
                writeln('=====DERET GEOMETRI=====');
                write('Masukan mau suku ke berapa (n) : '); readln(nilai[3].suku_ke);
                write('Masukan Suku awal          (a): '); readln(nilai[3].suku_awal);
                write('Masukan Rasio nya          (r): '); readln(nilai[3].pola_suku);
                hasil:=deret_geometri(nilai[3].suku_ke,nilai[3].suku_awal,nilai[3].pola_suku); //masuk ke function sekaligus mengisialisasi nilainya
                writeln;
                tabel;
                gotoxy(60,6);writeln('Suku ke-',nilai[3].suku_ke,' dengan nilai ',hasil:0:2); //ini hasilnya
            end
//====================================================================================================
//==============================PROGRAM UTAMA BARIS GEOMETRI==========================================
            else if pilih = 2 then 
            begin
                writeln;
                writeln('=====BARIS GEOMETRI=====');
                write('Masukan mau suku ke berapa (n): '); readln(nilai[4].suku_ke);
                write('Masukan Suku awal          (a): '); readln(nilai[4].suku_awal);
                write('Masukan Pola nya           (r): '); readln(nilai[4].pola_suku);
                hasil:=baris_geometri(nilai[4].suku_ke,nilai[4].suku_awal,nilai[4].pola_suku); //masuk ke function sekaligus mengisialisasi nilainya
                writeln;
                tabel;
                gotoxy(60,6);writeln('Suku ke-',nilai[4].suku_ke,' dengan nilai ',hasil:0:2); //ini hasilnya
            end
//====================================================================================================
            else if pilih = 3 then
            begin
                goto keluar; //kembali ke program utama
            end
            else
            begin
                exit; //kalau gak milih kembali program nya berhenti
            end
        end
//====================================================================================================
    else if pilih_mana = 3 then
    begin
        exit; //keluar dari program
    end
    else
        begin
            gotoxy(80,5);writeln('=========\(^_^)/========');
            gotoxy(80,6);writeln('========================');
            gotoxy(80,7);writeln('==                    ==');
            gotoxy(80,8);writeln('==         SOON       ==');
            gotoxy(80,9);writeln('==                    ==');
            gotoxy(80,10);writeln('========================');
            delay(1000); //untuk delay 1000 milidetik (1 detik) biar gak langsung kembali
            goto keluar; //kembali
        end;
    gotoxy(1,12);write('Mau Ulang Y/y ? '); readln(ulang);
    until (ulang <> 'Y') and (ulang <> 'y'); //untuk perulangan
end.
