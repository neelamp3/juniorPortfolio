# juniorPortfolio
junior


class PortfolioProject:
    def __init__(self, name):
        self.name = name
        self.scores = {
            "Code Quality and Functionality": 0,
            "Project Scope and Complexity": 0,
            "Documentation and Presentation": 0,
            "Version Control and Collaboration": 0,
            "Bonus Points": 0
        }

    def rate_code_quality(self):
        print("\nRate Code Quality and Functionality (0-10):")
        self.scores["Code Quality and Functionality"] = int(input(
            "How well does the code adhere to proper indentation, formatting, and meet the project requirements? (0-10): "))
        
        # Can also add more specific checks if desired
        # e.g. unit test coverage, error handling, etc.

    def rate_project_scope(self):
        print("\nRate Project Scope and Complexity (0-10):")
        self.scores["Project Scope and Complexity"] = int(input(
            "Does the project showcase a range of skills and tackle real-world problems? (0-10): "))

    def rate_documentation(self):
        print("\nRate Documentation and Presentation (0-10):")
        self.scores["Documentation and Presentation"] = int(input(
            "How well is the project documented? Is it easy to follow the setup and understand the code? (0-10): "))

    def rate_version_control(self):
        print("\nRate Version Control and Collaboration (0-10):")
        self.scores["Version Control and Collaboration"] = int(input(
            "Did you use Git effectively for version control? Did you collaborate or contribute to open-source? (0-10): "))

    def rate_bonus_points(self):
        print("\nRate Bonus Points (0-10):")
        self.scores["Bonus Points"] = int(input(
            "Did you deploy the project? Does it include advanced concepts like machine learning, live apps, etc.? (0-10): "))

    def display_project_summary(self):
        print(f"\nSummary for {self.name}:")
        for category, score in self.scores.items():
            print(f"{category}: {score}/10")
        print(f"Total score: {sum(self.scores.values())}/50")

def assess_portfolio():
    print("Welcome to the Python Portfolio Self-Assessment Tool!")
    project_name = input("\nEnter the name of your project: ")
    project = PortfolioProject(project_name)

    project.rate_code_quality()
    project.rate_project_scope()
    project.rate_documentation()
    project.rate_version_control()
    project.rate_bonus_points()

    project.display_project_summary()

if __name__ == "__main__":
    assess_portfolio()

