# NumberWizard---UdemyCourse

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class NumberWizard : MonoBehaviour

{

    int max = 1000;
    int min = 1;
    int tebakan = 500;

    void Start()
    {
        Debug.Log("Halooo, selamat datang di game sederhana pertama saya Number Wizard by Udemy");
        Debug.Log("Pilih nomor anda dan jangan beri tahu saya");
        Debug.Log("Angka tertinggi yang bisa anda pilih adalah : " + max);
        Debug.Log("Angka terendah yang bisa anda pilih adalah : " + min);
        Debug.Log("Beri tahu saya jika nomor anda lebih tinggi atau lebih rendah dari " + tebakan);
        Debug.Log("Tombol atas = tertinggi, Tombol bawah = terendah, Tekan Enter = kembali");
        max = max + 1;
    }

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.UpArrow))
        {
            min = tebakan;
            tebakan = (max + min) / 2;
            Debug.Log("Apakah nomor anda lebih besar atau lebih kecil dari = " + tebakan + " ?");
            Debug.Log(tebakan);
        }
        else if (Input.GetKeyDown(KeyCode.DownArrow))
        {
            max = tebakan;
            tebakan = (max + min) / 2;
            Debug.Log("Apakah nomor anda lebih besar atau lebih kecil dari = " + tebakan + " ?");
            Debug.Log(tebakan);
        }
        else if (Input.GetKeyDown(KeyCode.Return))
        {
            Debug.Log("Tombol kembali ditekan");
        }
    }
}
