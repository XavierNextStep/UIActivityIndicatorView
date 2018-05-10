# UIActivityIndicatorView
活动指示器知识点梳理
https://developer.apple.com/documentation/uikit/uiactivityindicatorview?language=objc
	UIActivityIndicatorView:
	Class（类）：
	A view that shows that a task is in progress.(一个显示当前正在进行的任务view。)
	Overview:
	You control when an activity indicator animates by calling the starAnimating and stopAnimating methhods.To automatically hide the activity indicator when animation stops,set the hidesWhenStopoed property to yes.(通过调用starAnimating和stopAnimating方法来控制活动指示器。)设置hideWhenStopped属性为YES，当活动指示器停止隐藏。
You can color of the activity indicator by using the color property.(你可以通过color属性来设置活动指示器的颜色。)
Topics
	Initializing an Activity Indictor（初始化活动指示）：
	InitWithActiviryIndicatorStyle:
	Instance Method：（实例方法）：
	Initializes and returns an activity-indicator object.(初始化并返回一个activity-indicator对象。)
	Declaration:
	-(instancetype)initWithActivityIndicatorStyle:(UIActivityIndicatorViewStyle)style;
	Parameters(参数):
	Style：A constant that specifies the style of the object to be create.See UIActivityIndicatorViewStyle for descryptions of the style constans.(一个常量，指定要创建的对象的风格。看UIActivityIndicatorViewStyle描述风格的常数。)
	Return Value(返回值)：
	An initialized UIActivityIndicatorView objct or nil if the object couldn’t be created.(一个初始化的UIActivityIndicatorView对象，如果没被创建返回一个nil)。
	Discussion（讨论）：
	UIActivityIndicatorView sizes the returned instance according to the specified style.You can set and retrieve the style of a activity indicator through the activityIndicatorViewStyle property.(UIActivityIndicatorView大小返回实例根据指定的style。你可以设置和检索活动指示器的风格通过activityIndicatorViewStyle属性。)
	initWithFrame:
	Instance Method（实例方法）：
	Declaration(宣言):
	- (instancetype)initWithFrame:(CGRect)frame;
	initWithCoder:
	InstanceMethod(实例方法：)
	Declaration(宣言)：
	- (instancetype)initWithCoder:(NSCoder *)coder;
	Managing an Activity Indicator（管理活动指示器）:
	startAnimating
	instanceMethod(实例方法)：
	Starts the animation of the progress indicatort.(开始指示器进度的动画。)
	Duscussion(讨论)：
	When the progress indicator is animated,the gear spins to indicate indetermainate progress.The indicator is animated until stopAnimating.(齿轮旋转的时候表示活动指示器正在进行，直到stopAnimating被调用。)
	stopAnimating
	instance Method(实例方法)：
	stopAnimaating
	stop the animation of the progress indicator.(停止进度指示器的动画。)
	Declaration(宣言)：
	- (void)stopAnimating;
	Discussion(讨论):
	Call this method to stop the animation of the progresss indicator started with a call to startAnimating.When animating is stopped,the indicator is hidden,unless hidesWhenStopped is NO.(调用此方法柯诺停止调用startAnimating进度指示器。当动画停止时进度指示器将隐藏，除非设置hidesWhenStopped属性为NO。)
	animating
	instance Property（实例属性）：
	A Boolean value indicating whether the activity indicator is currently running its animation.(一个布尔表示当前活动指示器是否在运行它的动画。)
	Declaration(宣言):
	@property(nonatomic, readonly, getter=isAnimating) BOOL animating;
	hidesWhenStopped
	instance Property(实例属性)：
	A Boolean value that controls whether the receiver is hidden when the animation is stop.(一个布尔值，用于控制活动指示器停止时是否隐藏。)
	Declaration(宣言)：
	@property(nonatomic) BOOL hidesWhenStopped;
	Discussion(讨论)：
	If the value of this property is YES (the default),the receiver sets its hidden property(UIView) to YES when receiver is not animating.If the hidesWhenStop property is NO,the receiver is not hidden when animation stops.You stop an animating progress indicator with the stopAnimating method.(如果这个值YES（默认的是YES）,如果接收者不进行动画时接受者被隐藏。如果hidesWhenstop属性设置为NO。当接收者停止运行时被隐藏。)
	Configuring the Activity Indicator Appearance(配置活动指示器)：
	ActivityIndicatorViewStyle
	Instance Property(实例属性)：
	The basic appearance of the activity indicator.(活动指示器最基础的外观。)
	Declaration(宣言)：
	@property(nonatomic) UIActivityIndicatorViewStyle activityIndicatorViewStyle;
	Discussion(讨论)：
	See UIActivityIndicatorViewStyle for the available styles.The defaule value is UIActivityIndicatorStyleWhite.(查看UIActivityIndicatorViewStyle 样式 其默认值UIActivityIndicatorStyleWhite )
	Color
	Instance Property(实例属性):
	The color of the activity indicator.(活动指示器的颜色。)
	Declaration(宣言):
	@property(readwrite, nonatomic, strong) UIColor *color;
	Discussion（活动）：
	If you set a color for an activity indicator,it overrides the color provided by the activityIndicatorViewStyle property.(如果设置活动指示器此属性，它将覆盖activityIndicatorViewStyle属性提供的颜色。)
	Constants(常量)：
	UIActivityIndicatorViewStyle
	Enumeration(枚举)：
	The visual style of the progress indicator.(活动指示器的风格。)
	OverView
	You set the value of the activityIndicatorViewStyle property with these constans.(你设置activityIndicatorViewStyle属性的常量值。
)
	Topics
	Constants 
	UIActivityIndicatorViewStytleWhiteLage
	Enumeration Case(枚举案例)
	The lage white stytle of indicator.(大型白色风格指示器。)
	Declaration(宣言)：
	UIActivityIndicatorViewStyleWhiteLarge
	UIActivityIndicatorViewStyleWhite
	Enumeration Case(枚举案例)
	The standard while style of indicator (the default).(标准的白色风格指示器（默认）。)
	Declaration(宣言)：
	UIActivityIndicatorViewStyleWhite
	UIActivityIndicatorViewStyleGray
	Enumeration Case(枚举案例)
	The standard gray style of indicator.(标准的灰色指示器。)
	Declaration(宣言)：
	UIActivityIndicatorViewStyleGray
	Relationships(关系)
	Inherits From(继承)：
	UIView
	Conforms To (符合)：
	NSCoding


     






