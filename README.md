NAMA : ALYA SEFHIA EKA PUTRI

NIM : 312210108

KELAS : TI.22.B1

# LATIHAN CLASS MAHASISWA DENGAN SETTER DAN GETTER

Tutorial Membuatnya sebagai berikut :

Pertama download terlebih dahulu APK Visual Studio di pc kalian masing-masing, kemudian install setelah di install buka Apk nya, selanjutnya buat new project terlebih dahulu lalu pilih Console Aplication C# atur nama project yang kalian inginkan setelah itu simpan, kemudian isi codingan seperti di bawah ini

- Code public class pegawai :
  
      using System;
      namespace TUGAS_OOP_PER_6{
      
          public class Pegawai{
              private string _nama;
              private double _gajipokok;
      
              public void setNama(string paramNama)
              {
                  _nama = paramNama;
              }
              // ALYA SEFHIA EKA PUTRI 31220108
              public string getNama()
              {
                  return _nama;
              }
              public void setGajiPokok(double paramGaji)
              {
                  _gajipokok = paramGaji;
              }
              public double getGajiPokok()
              {
                  return _gajipokok;
              }
              public virtual void cetakInfo()
              {
                  Console.WriteLine("Pegawai : " + getNama());
                  Console.WriteLine("Gaji Pokok : " + getGajiPokok());
              }
        }

- Code public class manager :

            public class Manager : Pegawai{
            private double _tunjangan;
            public void setTunjangan(double paramTunjangan)
            {
                _tunjangan = paramTunjangan;
            }
            public double getTunjangan()
            {
                return _tunjangan;
            }
            public void cetakTunjangan()
            {
                Console.WriteLine("Tunjangan Anda : " + getTunjangan());
            }
            public virtual void cetakInfo()
            {
                Console.WriteLine("Pegawai : " + getNama());
                Console.WriteLine("Posisi Anda : Manager");
                Console.WriteLine("Gaji Pokok Anda : " + getGajiPokok());
            }
        }

- Code public clas programer

        public class Programmer : Pegawai
      {
          private double _bonus;
          public void setBonus(double paramBonus)
          {
              _bonus = paramBonus;
          }
          public double getBonus()
          {
              return _bonus;
          }
          public void cetakBonus()
          {
              Console.WriteLine("Bonus Anda : " + getBonus());
          }
          public virtual void cetakInfo()
          {
              Console.WriteLine("Pegawai : " + getNama());
              Console.WriteLine("Posisi Anda : Programmer");
              Console.WriteLine("Gaji Pokok Anda : " + getGajiPokok());
          }
      }

- Code class data : Isi data sesuai yang kalian inginkan

           // ALYA SEFHIA EKA PUTRI 31220108
          class Alya
          {
              static void Main(string[] args)
              {
                  Console.WriteLine("==========Pegawai Clas==========");
                  Pegawai pegawai = new Pegawai();
                  pegawai.setNama("MAE  Pegawai");
                  pegawai.setGajiPokok(2000000);
                  pegawai.cetakInfo();
      
                  Console.WriteLine("==========Manager Class=========");
                  Manager manager = new Manager();
                  manager.setNama("ALYA CANTIK Manager");
                  manager.setGajiPokok(2500000);
                  manager.setTunjangan(4000000);
                  manager.cetakInfo();
                  manager.cetakTunjangan();
      
                  Console.WriteLine("==========Programer Class========");
                  Programmer programmer = new Programmer();
                  programmer.setNama("ALYA CANTIK Programmer");
                  programmer.setGajiPokok(30000000);
                  programmer.setBonus(5000000);
                  programmer.cetakInfo();
                  programmer.cetakBonus();
              }
            }
          }

- Berikut adalah output nya :

  ![oop](https://github.com/AkuuAlyaaa/OOP_PER_6/assets/115520278/2105a741-61cf-41f9-bdd7-d36492c065bf)

Sekian, Terimakasih
