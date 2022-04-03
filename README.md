import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: MainPage(),
    );
  }
}

class MainPage extends StatelessWidget {
  const MainPage({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    var tinggi = MediaQuery.of(context).size.height;
    var lebar = MediaQuery.of(context).size.width;

    return Scaffold(
      appBar: AppBar(
        centerTitle: true,
        backgroundColor: Colors.transparent,
        title: Text("POSTTEST 1 ABY KURNIAWAN"),
        titleTextStyle: const TextStyle(
          color: Color.fromARGB(255, 255, 0, 0),
          fontWeight: FontWeight.bold,
          fontStyle: FontStyle.normal,
          fontSize: 20.0
        ),
      ),
      body: Container(
        margin: EdgeInsets.all(50),
        width: lebar / 1.3,
        height: tinggi/ 1.3,
        alignment: Alignment.center,
        transform: Matrix4.rotationZ(-0.1),
        decoration: BoxDecoration(
          borderRadius: BorderRadius.circular(100),
          gradient: LinearGradient(colors: [
            Color.fromARGB(255, 0, 255, 68),
            Color.fromARGB(255, 72, 0, 255),
          ], begin: Alignment.topRight, end: Alignment.bottomLeft
          ),
          color: Colors.green,
          border: Border.all(
            width: 5,
            color: Colors.black,
          ),
        ),
        child: const Text(
          "Aby Kurniawan",
          style: TextStyle(
            fontSize: 25,
            fontWeight: FontWeight.bold,
            color: Color.fromARGB(255, 255, 234, 0),
          ),
        ),
      ),
    );
  }
}
