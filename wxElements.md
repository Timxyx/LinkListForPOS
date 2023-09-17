## wxWidgets UI Elements Cheat Sheet

### 1. Basic Elements:

#### Button:
```cpp
wxButton* btn = new wxButton(parent, ID, "Label", wxDefaultPosition, wxDefaultSize);
```
- Methods:
  - `btn->Enable(bool enable)`
  - `btn->SetLabel("New Label")`

#### Text Control:
```cpp
wxTextCtrl* txtCtrl = new wxTextCtrl(parent, ID, "", wxDefaultPosition, wxDefaultSize);
```
- Methods:
  - `txtCtrl->GetValue()`
  - `txtCtrl->SetValue("New Text")`
  - `txtCtrl->AppendText("Additional Text")`

#### Static Text:
```cpp
wxStaticText* lbl = new wxStaticText(parent, wxID_ANY, "Label");
```

### 2. Selection Elements:

#### Choice (Dropdown):
```cpp
wxChoice* choice = new wxChoice(parent, ID, wxDefaultPosition, wxDefaultSize, arrayStringChoices);
```
- Methods:
  - `choice->GetSelection()`
  - `choice->SetSelection(int n)`
  - `choice->GetString(int n)`

#### ComboBox:
```cpp
wxComboBox* combo = new wxComboBox(parent, ID, "", wxDefaultPosition, wxDefaultSize, arrayStringChoices);
```
- Methods:
  - `combo->GetValue()`
  - `combo->SetValue("New Text")`
  - `combo->GetSelection()`
  - `combo->SetSelection(int n)`

#### ListBox:
```cpp
wxListBox* listbox = new wxListBox(parent, ID, wxDefaultPosition, wxDefaultSize, arrayStringChoices);
```
- Methods:
  - `listbox->GetSelection()`
  - `listbox->SetString(int n, "New String")`
  - `listbox->Append("New Item")`

### 3. Containers:

#### Panel:
```cpp
wxPanel* panel = new wxPanel(parent, ID);
```

#### Notebook:
```cpp
wxNotebook* notebook = new wxNotebook(parent, ID);
```
- Methods:
  - `notebook->AddPage(panel, "Tab Label")`
  - `notebook->GetSelection()`
  - `notebook->SetSelection(int n)`
