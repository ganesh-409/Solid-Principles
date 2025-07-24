package com.principles;

class User {
	private String name;

	public User(String name) {
		this.name = name;
	}

	public String getName() {
		return name;
	}
}

//Separate class with single responsibility: printing user info
public class Single_Res {
	public void printUser(User user) {
		System.out.println("User name: " + user.getName());
	}
}
package com.principles;

interface Workable {
	void work();
}

interface Eatable {
	void eat();
}

class Developer implements Workable, Eatable {
	public void work() {
		System.out.println("Developer working");
	}

	public void eat() {
		System.out.println("Developer eating");
	}
}

class Robot implements Workable {
	public void work() {
		System.out.println("Robot working");
	}
}

public class Interface_Segr {
	public static void main(String[] args) {
		Developer dev = new Developer();
		dev.work();
		dev.eat();

		Robot bot = new Robot();
		bot.work();
	}
}package com.principles;

abstract class Bird {
	abstract void eat();
}

class Sparrow extends Bird {
	@Override
	void eat() {
		System.out.println("Sparrow is eating");
	}
}

class Crow extends Bird {
	@Override
	void eat() {
		System.out.println("Crow is eating");
	}
}

public class Liskon_Sub {
	public static void main(String[] args) {
		Bird bird1 = new Sparrow();
		Bird bird2 = new Crow();

		bird1.eat();
		bird2.eat();
	}
}
package com.principles;

interface Hospital {
	void activity();
}

class Doctor implements Hospital {
	public void activity() {
		System.out.println("Doctor done with heart surgery");
	}
}

class Patient implements Hospital {
	public void activity() {
		System.out.println("make pay payment");
	}
}

class Counter {
	void process(Hospital hos_method) {
		hos_method.activity();
	}
}

public class Open_Closed {
	public static void main(String[] args) {
		Counter p = new Counter();
		p.process(new Patient());
		p.process(new Doctor());
	}
}package com.principles;

class User {
	private String name;

	public User(String name) {
		this.name = name;
	}

	public String getName() {
		return name;
	}
}

//Separate class with single responsibility: printing user info
public class Single_Res {
	public void printUser(User user) {
		System.out.println("User name: " + user.getName());
	}
}
