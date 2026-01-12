🔹 What is Auth Guard in Angular?
✅ Definition (Best Interview Answer)

Auth Guard is an Angular feature used to protect routes by checking whether a user is authenticated or authorized before allowing navigation.

If the condition fails, Angular blocks the route or redirects the user (usually to a login page).

🔹 Why do we use Auth Guard?

Prevent unauthorized access

Secure pages like Dashboard, Admin, Profile

Control role-based access

🔹 Types of Route Guards
Guard	Purpose
CanActivate	Allow/deny route access
CanActivateChild	Protect child routes
CanDeactivate	Prevent leaving a page
Resolve	Load data before route
CanLoad	Prevent lazy module loading
🔹 Simple Auth Guard Example
@Injectable({ providedIn: 'root' })
export class AuthGuard implements CanActivate {

  canActivate(): boolean {
    return !!localStorage.getItem('token');
  }
}

const routes: Routes = [
  { path: 'dashboard', component: DashboardComponent, canActivate: [AuthGuard] }
];
🔹 What is ChangeDetector in Angular?
✅ Definition (Best Interview Answer)

Change Detector is Angular’s mechanism that detects changes in component data and updates the DOM automatically.

It keeps the view synchronized with the model.

🔹 How Change Detection Works

Angular runs change detection after:

User events (click, input)

HTTP responses

Timers (setTimeout)

Uses Zone.js (traditional approach)

Compares old and new values and updates the UI

🔹 Change Detection Strategies
Strategy	Description
Default	Checks entire component tree
OnPush	Checks only when input changes
🔹 Example: OnPush Change Detection
@Component({
  selector: 'app-demo',
  changeDetection: ChangeDetectionStrategy.OnPush
})
export class DemoComponent {
  @Input() data: string;
}


✔ Improves performance
✔ Reduces unnecessary checks

🔹 Manually Trigger Change Detection
constructor(private cd: ChangeDetectorRef) {}

this.cd.detectChanges();

🔹 One-Line Interview Answer

Change Detector automatically updates the UI when component data changes.

🔹 Difference (Quick Comparison)
Auth Guard	Change Detector
Used for routing security	Used for UI updates
Controls navigation	Controls DOM rendering
Runs before route loads	Runs during app lifecycle

🔥 Interview Tip (Important)

If interviewer asks:

How does Angular improve performance?

Answer:

By using OnPush change detection, lazy loading, and route guards to control rendering and navigation.
