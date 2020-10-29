	public static void main(String[] args) {
		Scanner sc = new Scanner (System.in);
		System.out.print("Введите URL-адрес: ");
		String s = sc.next();
		Pattern pattern = Pattern.compile("^(https?:\\/\\/)?([\\da-z\\.-]+)\\.([a-z\\.]{2,6})([\\/\\w\\.-]*)?(ru|com|su|org)*\\/?$");
		Matcher matcher = pattern.matcher(s);
		if (matcher.matches()) {
			System.out.println("Введенный URL-адресс - корректный");
		}
		else {
			System.out.println("Введенный URL-адресс - некорректный.Предлагаем проверить правильность написанного URL-адреса!");
		}
	}

}
