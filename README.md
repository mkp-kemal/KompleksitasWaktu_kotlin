import kotlin.system.measureTimeMillis

fun hitungRerata(a: IntArray): Double {
    var jumlah = 0.0
    for (i in a.indices) {
        jumlah += a[i]
    }
    return jumlah / a.size
}

fun main() {
    print("Masukkan banyak data: ")
    val n = readLine()!!.toInt()

    val a = IntArray(n)
    for (i in 0 until n) {
        print("Masukkan data ke-${i+1}: ")
        a[i] = readLine()!!.toInt()
    }

    val time = measureTimeMillis {
        val rataRata = hitungRerata(a)
        println("Nilai rata-rata: $rataRata")
    }

    println("Waktu eksekusi: $time millisecond")
}
