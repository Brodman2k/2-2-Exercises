# 2-2 Exercises

This IntelliJ IDEA project contains three introductory Java exercises that practice console output, method calls, and basic debugging.

## Exercises

- [`Text01.java`](src/Text01.java) prints an ASCII-art animal face using `System.out.println()` statements and escaped backslashes.
- [`Text02.java`](src/Text02.java) prints the numbers `1` through `4`, with each number on a separate line.
- [`Text03.java`](src/Text03.java) builds on `Text01` by moving the leg output into a reusable `drawLegs()` method and calling it from `main()`.

## Requirements

- A Java Development Kit (JDK)
- IntelliJ IDEA, or a terminal that can run `javac` and `java`

## Run in IntelliJ IDEA

1. Open the project in IntelliJ IDEA.
2. Open one of the files in the `src` directory.
3. Click the green Run icon next to the class or its `main()` method.
4. Select **Run** to view the program's output.

## Compile and run from a terminal

From the project directory, compile all three classes:

```powershell
New-Item -ItemType Directory -Force -Path out/classes | Out-Null
javac -d out/classes src/Text01.java src/Text02.java src/Text03.java
```

Run an individual exercise:

```powershell
java -cp out/classes Text01
java -cp out/classes Text02
java -cp out/classes Text03
```

## Debug `Text03`

1. Open `src/Text03.java`.
2. Set a breakpoint on Line 11 by clicking in the gutter beside the line number.
3. Click the Debug icon next to `main()` or select **Debug 'Text03.main()'**.
4. Execution will pause on Line 11.
5. Resume or step through the program until Line 19, where `drawLegs ();` is called.
6. Step into the call to follow execution into the `drawLegs()` method.

## Expected `Text03` output

```text
   /\         /\
  /  \_______/  \
 /               \
(  /\         /\  )
====     V     ====
======(__|__)======
  (             )
   (___________)
     ||     ||
     ||     ||
    (||)   (||)
```
