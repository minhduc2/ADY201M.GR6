import PySimpleGUI as sg

layout = [
    [sg.Text("Enter employer", background_color="green", text_color="yellow", justification="left")],
    [sg.InputText()],
    [sg.Button("Submit")]
]

window = sg.Window("Automated Data Entry Form", layout)

while True:
    event, values = window.read()
    if event == sg.WIN_CLOSED:
        break
    if event == "Submit":
        employer_name = values[0]
        # Do something with the employer name, e.g., store it or process it
        sg.popup(f"Employer Name: {employer_name}", title="Submitted")

window.close()
