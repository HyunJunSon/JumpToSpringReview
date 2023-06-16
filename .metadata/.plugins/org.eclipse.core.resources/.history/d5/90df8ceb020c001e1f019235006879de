package com.mysite.sbb.question;

import java.util.List;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;

import lombok.RequiredArgsConstructor;

@Controller
@RequiredArgsConstructor
class QuestionController {

	private final QuestionService questionService;
	
    @GetMapping("/question/list")
    public String list(Model model) {
    	
    	List<Question> questionList = this.questionService.getList();
    	
    	model.addAttribute("questionList", questionList);
    	
        return "question_list";
    }
    
    @GetMapping("/question/leaf")
    public String list2(Model model) {
    	
    	model.addAttribute("questionList", this.questionRepository.findAll());
    	
    	return "leafTest";
    }
}
