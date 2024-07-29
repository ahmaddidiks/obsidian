Core concept React
- Component
- Props
- State

### Apa itu component
- UI dipecah menjadi bagian-bagian kecil yang disebut komponen
- Dengan begitu kita bisa membuat module komponen yang re-useable yang bisa di gabung2kan menjadi bagian yang lebih besar
- Misalkan komponen image, deskripsi, button ==> yang digabung menjadi bagian
- Komponen pada React sejatinya adalah function
- nama function ditulis dengan awalan huruf Besar
- Function mengembalikan elemen UI yang akan dijadikan komponen, ditulis dengan jsx
- dipanggil sbg tag HTML saat dirender
- Contohnya:

```js
<script type="text/babel">
	const container = document.getElementById('root')
	const root = ReactDOM.createRoot(container);
	
	function Header() {
		return ( <h1>Belajar React bareng WPU</h1> )
	}

	function HomePage() {
		return (
			<div>
				<Header />
				<Header />
				<Header />
			</div>
		)
	}

	root.render(<HomePage />);
</script>
```

Komponen selain reuseable, bisa dijadikan dinamis. Jika ingin membuat komoponen menjadi dinamis (menggunakan komponen yang sama, namun menampilkan informasi yang berbeda) maka memerlukan Props.

### Apa itu props
- Mengirim properti sbg informasi ke komponen yang disebut Props.
- Props  dianggap sbg obejct di komponen
- Contoh: 
```js
<script type="text/babel">
	const container = document.getElementById('root')
	const root = ReactDOM.createRoot(container);
	
	function Greeting(props) {
		return ( <h1>Hallo {props.name}</h1> )
	}

	function HomePage() {
		return (
			<div>
				<Greeting name="Didik"/>
				<Greeting name="Ahmad"/>
			</div>
		)
	}

	root.render(<HomePage />);
</script>
``` 

- Props refactoring:
- Props perulangan


Jika ingin menambah interaksi, maka melakukannya dengan state
### Apa itu state
- banayak hal yang bisa berubah karena interaksi dilakukan user
- Data yang berubah-ubah tersebut disebut state
- Selain state, untuk menambah interaktivitas juga menggunakn Event Handler
- State dan Hook
- Misalakan membuat tombol yang jika diklik akan menambahkan jumlah angka berapa kali tombol diklik
- Hooks adalah function untuk menambah logic pada react untuk mengelola state
- Misalakna setState() --> Mengelola state yang mengembalikan nilai berupa array. Teknik ini disebut destructering
- Element pertama dari array adalah nilai state, kedua merupakan function untuk mengubah nilainya.
- 