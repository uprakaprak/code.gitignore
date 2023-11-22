print("=====================================")
print("| Aplikasi perhitungan gaji DEV-JOS |")
print("=====================================\n")
print("--------------")
print("Daftar jabatan")
print("--------------")
print("1. Junior Web Programmer")
print("2. Senior Web Programmer")
print("3. UI Designer")
print("4. Database Administrator\n")


print("-------------")
print("Masukkan Data")
print("-------------")

nip =      int(input("Masukkan NIP  : "))
nama =     input    ("Nama karyawan : ")
jabatan =  int(input("Jabatan       : "))
jam =      int(input("Jam kerja     : "))

if jabatan == 1:
   jab = "Senior programmer"
   gaji= 300000
elif jabatan == 2:
   jab = "junior web programmer"
   gaji= 200000
elif jabatan == 3:
   jab = "UI disigner"
   gaji= 150000
elif jabatan == 4:
    jab = "Database administrator"
    gaji= 250000

#upah lembur 50rb/menit
upah_lembur = 100000

#menghitung jam lembur
if jam > 40:
   jam_lembur = jam - 40
elif jam < 40:
   jam_lembur = 0

#menghitung gaji pokok
gaji_pokok = (jam - jam_lembur) * gaji
gaji_lembur = jam_lembur * upah_lembur
total_gaji = gaji_pokok + gaji_lembur

print("\n-----------------")
print("Hasil Perhitungan")
print("-----------------")
print("NIP           :",nip)
print("Nama Karyawan :",nama)
print("Jabatan       :",jab)
print("jam kerja     :",jam,"jam")
print("gaji pokok    :","Rp",gaji_pokok,)
print("lembur        :",jam_lembur,"jam")
print("upah lembur   :","Rp",gaji_lembur)
print("total gaji    :","Rp",total_gaji)

print("\n..==Terima Kasih==..")
