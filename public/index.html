<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aplikasi Perpustakaan Sederhana</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100 min-h-screen py-10 px-4">
    <div class="max-w-2xl mx-auto bg-white shadow-md rounded-lg p-6">
        <h1 class="text-2xl font-bold text-gray-800 mb-6 text-center">📚 Perpustakaan Digital</h1>

        <!-- Form Tambah Buku -->
        <form id="bookForm" class="mb-8 bg-gray-50 p-4 rounded-md border">
            <h2 class="text-lg font-semibold mb-3 text-gray-700">Tambah Buku Baru</h2>
            <div class="grid grid-cols-1 gap-3 sm:grid-cols-3 mb-3">
                <input type="text" id="title" placeholder="Judul Buku" required class="border p-2 rounded focus:outline-none focus:ring-2 focus:ring-blue-400">
                <input type="text" id="author" placeholder="Penulis" required class="border p-2 rounded focus:outline-none focus:ring-2 focus:ring-blue-400">
                <input type="number" id="year" placeholder="Tahun Terbit" class="border p-2 rounded focus:outline-none focus:ring-2 focus:ring-blue-400">
            </div>
            <button type="submit" class="w-full bg-blue-600 text-white p-2 rounded hover:bg-blue-700 transition">Simpan Buku</button>
        </form>

        <!-- Daftar Buku -->
        <h2 class="text-lg font-semibold mb-3 text-gray-700">Daftar Buku</h2>
        <div id="loading" class="text-center text-gray-500 py-4">Memuat data...</div>
        <div class="overflow-x-auto">
            <table class="w-full border-collapse border border-gray-200 hidden" id="bookTable">
                <thead>
                    <tr class="bg-gray-100">
                        <th class="border border-gray-200 p-2 text-left">Judul</th>
                        <th class="border border-gray-200 p-2 text-left">Penulis</th>
                        <th class="border border-gray-200 p-2 text-center">Tahun</th>
                        <th class="border border-gray-200 p-2 text-center">Aksi</th>
                    </tr>
                </thead>
                <tbody id="bookList">
                    <!-- Data akan dimuat lewat JavaScript -->
                </tbody>
            </table>
        </div>
    </div>

    <script>
        const bookForm = document.getElementById('bookForm');
        const bookTable = document.getElementById('bookTable');
        const bookList = document.getElementById('bookList');
        const loading = document.getElementById('loading');

        async function fetchBooks() {
            try {
                const res = await fetch('/api/books');
                const result = await res.json();
                
                loading.style.display = 'none';
                if (result.success && result.data.length > 0) {
                    bookTable.classList.remove('hidden');
                    bookList.innerHTML = '';
                    result.data.forEach(book => {
                        const row = document.tr = document.createElement('tr');
                        row.innerHTML = `
                            <td class="border border-gray-200 p-2">${book.title}</td>
                            <td class="border border-gray-200 p-2">${book.author}</td>
                            <td class="border border-gray-200 p-2 text-center">${book.year}</td>
                            <td class="border border-gray-200 p-2 text-center">
                                <button onclick="deleteBook('${book.id}')" class="bg-red-500 text-white px-3 py-1 rounded text-sm hover:bg-red-600">Hapus</button>
                            </td>
                        `;
                        bookList.appendChild(row);
                    });
                } else {
                    bookList.innerHTML = `<tr><td colspan="4" class="text-center p-4 text-gray-500">Belum ada buku di perpustakaan.</td></tr>`;
                    bookTable.classList.remove('hidden');
                }
            } catch (err) {
                loading.textContent = 'Gagal memuat data buku.';
            }
        }

        bookForm.addEventListener('submit', async (e) => {
            e.preventDefault();
            const title = document.getElementById('title').value;
            const author = document.getElementById('author').value;
            const year = document.getElementById('year').value;

            const res = await fetch('/api/books', {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ title, author, year })
            });

            const result = await res.json();
            if (result.success) {
                bookForm.reset();
                fetchBooks();
            } else {
                alert('Gagal menambah buku: ' + result.message);
            }
        });

        async function deleteBook(id) {
            if (confirm('Yakin ingin menghapus buku ini?')) {
                const res = await fetch(`/api/books/${id}`, { method: 'DELETE' });
                const result = await res.json();
                if (result.success) {
                    fetchBooks();
                } else {
                    alert('Gagal menghapus buku');
                }
            }
        }

        fetchBooks();
    </script>
</body>
</html>