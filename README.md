# SessionMgntSpringMvc

1.Model

@Component
@Scope("session")
public class SessionUser {
	String user;
	public String getUser() {
		return user;
	}
	public void setUser(String user) {
		this.user = user;
	}
}

2.Controller
@Scope("session")
@RestController
public class HomeController {

@Autowired
private SessionUser sess_user;

// use this section on any method....
sess_user.setUser(pname);
mv=new ModelAndView("index");
mv.addObject("sess_user",pname);

//get session..
 logger.info("User :: "+ sess_user.getUser());
		    
		    

}
