# kuli-ah

@Composable
fun ImageAndTextCard() {
    Card(
        modifier = Modifier
            .fillMaxWidth()
            .padding(16.dp),
        elevation = 8.dp,
        shape = RoundedCornerShape(8.dp)
    ) {
        Column(
            modifier = Modifier.padding(16.dp)
        ) {
            // Gambar
            Image(
                painter = painterResource(id = R.drawable.sample_image),
                contentDescription = "Sample Image",
                modifier = Modifier
                    .fillMaxWidth()
                    .height(200.dp)
                    .clip(RoundedCornerShape(8.dp)),
                contentScale = ContentScale.Crop
            )

            Spacer(modifier = Modifier.height(8.dp))

            // Teks
            Text(
                text = "Judul Kartu",
                style = MaterialTheme.typography.h6,
                modifier = Modifier.padding(bottom = 4.dp)
            )
            Text(
                text = "Deskripsi singkat tentang kartu ini yang memberikan lebih banyak informasi kepada pengguna.",
                style = MaterialTheme.typography.body2
            )
        }
    }
}
