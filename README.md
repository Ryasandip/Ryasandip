import java.util.Scanner;

class Belajar_method {
    // Deklarasi atribut dengan access modifier private
    private String nama;
    private String alamat;
    private int tlp;
    private int daftar;
    private int obat;
    private int vitamin;

    // Method untuk meminta input data pasien
    public void data() {
        System.out.println("\nNama Pasien\t\t\t\t: " + nama);
        System.out.println("Alamat Pasien\t\t\t\t: " + alamat);
        System.out.println("No. Tlp pasien \t\t \t\t: +62" + tlp);
    }

    // Method untuk menghitung total biaya administrasi
    public int administrasi() {
        int total = daftar + obat + vitamin;
        return total;
    }

    // Method utama (main)
    public static void main(String[] xx) {
        // Membuat objek Scanner untuk input
        Scanner test = new Scanner(System.in);
        // Membuat objek dari kelas Belajar_method
        Belajar_method a = new Belajar_method();

        // Meminta input data pasien
        System.out.print("Masukan Nama : \t\t\t");
        a.nama = test.nextLine();

        System.out.print("Masukan Alamat : \t\t\t");
        a.alamat = test.next();

        System.out.print("Masukan No. Tlp : \t\t\t+62");
        a.tlp = test.nextInt();

        System.out.print("Masukan Biaya Pendaftaran \t\tRp. ");
        a.daftar = test.nextInt();

        System.out.print("Masukan Biaya Obat \t\t\tRp. ");
        a.obat = test.nextInt();

        System.out.print("Masukan Biaya Vitamin \t\t\tRp. ");
        a.vitamin = test.nextInt();

        // Menampilkan data pasien
        a.data();

        // Menampilkan total biaya yang harus dibayar
        System.out.println("\nTotal Biaya yang di Bayar Pasien \tRp. " + a.administrasi());
    }
