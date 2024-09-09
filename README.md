from PyQt5.QtWidgets import (QPushButton, QRadioButton, QLabel, QApplication, QSpinBox, QGroupBox, QButtonGroup, QHBoxLayout, QVBoxLayout)
from PyQt5.QtCore import Qt

app = QApplication([])

btn_menu = QPushButton("Меню")
btn_rest = QPushButton("Відпочити")
spin = QSpinBox()
spin.setValue(30)

lable1 = QLabel("Apple")
lable2 = QLabel("Milk")
lable3 = QLabel("Juice")
lable4 = QLabel("Apple")

main_line_quizz = QVBoxLayout()
line1_quizz = QHBoxLayout()

main_line_quizz.addWidget(lable1, alignment=Qt.AlignRight)
main_line_quizz.addWidget(lable2, alignment=Qt.AlignRight)

line1_quizz.addWidget(lable3, alignment=Qt.AlignLeft)
line1_quizz.addWidget(lable4, alignment=Qt.AlignLeft)

line1_quizz.addWidget(btn_menu)
line1_quizz.addStretch(1)
line1_quizz.addWidget(btn_rest)
line1_quizz.addWidget(spin)
line1_quizz.addWidget(QLabel("хвилин"))

main_line_quizz.addLayout(line1_quizz)
