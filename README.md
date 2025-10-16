

---

# 🔍 Word Finder — Words Starting with "t" or "m"

A **C# Windows Forms Application** built in **Visual Studio 2022** that uses **Regular Expressions (Regex)** to find and display all the words in a text that start with the letters **‘t’** or **‘m’** (case-insensitive).

---

## 🚀 Features

* ✅ Detects all words starting with **t** or **m** (uppercase or lowercase)
* 🧠 Uses **Regex** for efficient pattern matching
* 🪟 Displays results in a separate output box (`TextBox2`)
* ❌ Shows a message if no matching words are found
* 💡 Simple, user-friendly GUI built with **Windows Forms**

---

## 🧠 Regular Expression Used

```regex
\b[tT]\w*\b|\b[mM]\w*\b
```

### Explanation

| Part      | Meaning                                                         |                              |
| --------- | --------------------------------------------------------------- | ---------------------------- |
| `\b`      | Word boundary (ensures match starts at the beginning of a word) |                              |
| `[tT]`    | Matches lowercase or uppercase **t**                            |                              |
| `\w*`     | Matches the rest of the word (letters, digits, underscores)     |                              |
| `         | `                                                               | OR (for alternate condition) |
| `[mM]\w*` | Matches lowercase or uppercase **m**                            |                              |

---

## 🧩 Example Input

```
The moon travels through the misty mountains in the morning.
```

### ✅ Output

```
The
moon
travels
through
the
misty
mountains
morning
```

---

## 🧮 Code Snippet

```csharp
Regex regex = new Regex(@"\b[tT]\w*\b|\b[mM]\w*\b");
MatchCollection matches = regex.Matches(textBox1.Text);

textBox2.Clear();

if (matches.Count > 0)
{
    foreach (Match match in matches)
    {
        textBox2.AppendText(match.Value + Environment.NewLine);
    }
}
else
{
    MessageBox.Show("No words found starting with 't' or 'm'.");
}
```

---

## 🖥️ How It Works

1. User enters or pastes a paragraph into **TextBox1**.
2. Click the **Find Words** button.
3. The program finds all words that start with **‘t’** or **‘m’**.
4. The results appear in **TextBox2**, each on a new line.

---

## ⚙️ Setup Instructions

1. Open **Visual Studio 2022**.
2. Create a new project → **Windows Forms App (.NET Framework)**.
3. Add two text boxes (`textBox1`, `textBox2`) and a button (`button1`).
4. Copy and paste the provided code into `Form1.cs`.
5. Press **F5** to run the project.
6. Enter some text and click the button to test.

---

## 📂 Project Structure

```
📦 WordFinderApp
 ┣ 📜 Form1.cs
 ┣ 📜 Form1.Designer.cs
 ┣ 📜 Program.cs
 ┗ 📜 README.md
```

---

## 💡 Future Improvements

* Allow user to choose starting letters dynamically.
* Highlight matching words directly in the text.
* Support word frequency count.

---

## 🧑‍💻 Author

**Muhammad Haseeb**
🎓 Computer Science Student

---

