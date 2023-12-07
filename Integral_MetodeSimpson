def f(x):
    # Definisikan fungsi yang ingin diintegrasikan di sini
    return x**2  # Contoh: fungsi x^2

def simpson_one_third(a, b, n):
    """
    Menghitung integral menggunakan metode Simpson 1/3

    Parameters:
    a (float): Batas bawah integral
    b (float): Batas atas integral
    n (int): Jumlah subinterval (harus genap)

    Returns:
    hasil_integral (float): Nilai integral
    """

    if n % 2 != 0:
        raise ValueError("Jumlah subinterval harus genap")

    h = (b - a) / n
    x = [a + i * h for i in range(n+1)]
    y = [f(x[i]) for i in range(n+1)]

    integral = y[0] + y[n]  # Penjumlahan ujung pertama dan terakhir

    # Penjumlahan untuk bagian genap
    for i in range(1, n, 2):
        integral += 4 * y[i]

    # Penjumlahan untuk bagian ganjil
    for i in range(2, n-1, 2):
        integral += 2 * y[i]

    hasil_integral = integral * h / 3

    return hasil_integral

# Memasukkan nilai dari pengguna
batas_bawah = float(input("Masukkan nilai batas bawah integral: "))
batas_atas = float(input("Masukkan nilai batas atas integral: "))
jumlah_subinterval = int(input("Masukkan jumlah subinterval (harus genap): "))

# Menghitung integral menggunakan metode Simpson 1/3
integral_hasil = simpson_one_third(batas_bawah, batas_atas, jumlah_subinterval)
print(f"Hasil integral menggunakan metode Simpson 1/3: {integral_hasil}")
