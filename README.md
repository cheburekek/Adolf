






class TestWin(QWidget):
    def __init__(self):
        #self.setStyleSheet(cur)
        super().__init__()
        self.set_appear()
        self.initUI()
        self.connects()
        self.show()

    def set_appear(self):
        self.setWindowTitle(txt_title)
        self.resize(win_width, win_height)
        self.move(win_x, win_y)

    def initUI(self):
        '''создаёт графические элементы'''
        #self.questionnary = AllQuestions()
        self.btn_next = QPushButton(txt_sendresults, self)
        self.btn_test1 = QPushButton(txt_starttest1, self)
        self.btn_test2 = QPushButton(txt_starttest2, self)
        self.btn_test3 = QPushButton(txt_starttest3, self)
        self.text_name = QLabel(txt_name)
        self.text_age = QLabel(txt_age)
        self.text_test1 = QLabel(txt_test1)
        self.text_test2 = QLabel(txt_test2)
        self.text_test3 = QLabel(txt_test3)
        self.text_timer = QLabel(txt_timer)
        self.line_name = QLineEdit(txt_hintname)
        self.line_age = QLineEdit(txt_hintage)
        self.line_test1 = QLineEdit(txt_hinttest1)
        self.line_test2 = QLineEdit(txt_hinttest2)
        self.line_test3 = QLineEdit(txt_hinttest3)
        self.l_line = QVBoxLayout()
        self.r_line = QVBoxLayout()
        self.h_line = QVBoxLayout()
        self.l_line.addWidget(self.text_timer, aligment = Qt.AlignCenter)
        self.l_line.addWidget(self.text_name, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.line_name, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.text_age, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.line_age, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.text_test1, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.btn_test1, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.line_test1, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.text_test2, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.btn_test2, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.line_test2, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.text_test3, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.btn_test3, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.line_test3, aligment = Qt.Alignleft)
        self.l_line.addWidget(self.btn_text, aligment = Qt.AlignCenter)
        self.h_line.addLayout(self.l_line)
        self.h_line.addLayout(self.r_line)
        self.setLayout(self.h_line)

    def connects(self):
        self.btn_next.cliced.connect(self.next_click)

        def next_click(self):
            self.hide()
            self.fw = Fina_Win
        
        
        
