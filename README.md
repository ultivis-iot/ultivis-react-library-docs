# Ultivis React Library

## 📦 Installation

```bash
npm install @ultivis-iot/react
# or
yarn add @ultivis-iot/react
```

## 🚀 Quick Start

### 1. Setup AppProviders

```jsx
import { AppProviders } from '@ultivis-iot/react';
import { createBrowserRouter } from 'react-router-dom';
import '@ultivis-iot/react/styles';

const router = createBrowserRouter([
  // your routes
]);

function App() {
  return (
    <AppProviders
      router={router}
      favicon="/favicon.ico"
      brandLogo="/logo.png"
      navLogo="/nav-logo.png"
      login={true}
    />
  );
}

export default App;
```

### 2. Using Layout

```jsx
import { Layout } from '@ultivis-iot/react';

function MyPage() {
  return (
    <Layout
      headerItems={<></>}
      sidebarItems={<></>}
      pageTitle={() => 'My Page'}
    >
      {/* Page content */}
    </Layout>
  );
}
```

## 📚 Key Features

### 🎨 UI Components
Fully customizable components based on Radix UI

### 📊 Dashboard System
Dynamic widget-based dashboard creation and management

### 🔐 Authentication
Built-in authentication system and protected routes

### 🌍 Internationalization
Multi-language support based on i18next

### 🎯 IoT Device Management
Device tree and data management components

## 📦 Components

### Layout
- [`Layout`](./global.html#Layout) - Main layout component (header, sidebar, content area)
- [`Header`](./global.html#Header) - Application header
  - [`AppSwitcher`](./global.html#AppSwitcher) - Application switcher
  - [`AppSwitcherItem`](./global.html#AppSwitcherItem) - App switcher item
  - [`UserMenu`](./global.html#UserMenu) - User menu
  - [`UserMenuItem`](./global.html#UserMenuItem) - User menu item
  - [`HeaderDivider`](./global.html#HeaderDivider) - Header divider
- [`Sidebar`](./global.html#Sidebar) - Sidebar navigation
  - [`SidebarItem`](./global.html#SidebarItem) - Sidebar menu item
  - [`GroupAccordion`](./global.html#GroupAccordion) - Group accordion
  - [`SidebarAccordionItem`](./global.html#SidebarAccordionItem) - Sidebar accordion item
- [`MenuBar`](./global.html#MenuBar) - Menu bar
  - [`ActionBar`](./global.html#ActionBar) - Action bar
  - [`ActionItem`](./global.html#ActionItem) - Action item
  - [`TabItem`](./global.html#TabItem) - Tab item

### Form Fields
- [`FormInputField`](./global.html#FormInputField) - Text input field
- [`FormSelectField`](./global.html#FormSelectField) - Select field
- [`FormCheckboxField`](./global.html#FormCheckboxField) - Checkbox field
- [`FormSwitchField`](./global.html#FormSwitchField) - Switch field
- [`FormRadioField`](./global.html#FormRadioField) - Radio button field
- [`FormTextareaField`](./global.html#FormTextareaField) - Textarea field
- [`FormColorField`](./global.html#FormColorField) - Color picker field
- [`FormIconSelectField`](./global.html#FormIconSelectField) - Icon select field
- [`FormInputArrayField`](./global.html#FormInputArrayField) - Array input field
- [`EditableField`](./global.html#EditableField) - Editable field

### Dashboard
- [`ContextDashboard`](./global.html#ContextDashboard) - Dynamic context dashboard
- [`StaticDashboard`](./global.html#StaticDashboard) - Static dashboard
- [`DashboardTabs`](./global.html#DashboardTabs) - Dashboard tabs
- Dashboard Modals
  - [`DashboardModal`](./global.html#DashboardModal) - Dashboard settings modal
  - [`WidgetModal`](./global.html#WidgetModal) - Widget settings modal
  - [`SelectWidget`](./global.html#SelectWidget) - Widget selector
  - [`Configuration`](./global.html#Configuration) - Widget configuration
  - [`PreviewWidget`](./global.html#PreviewWidget) - Widget preview
  - [`RemoveModal`](./global.html#RemoveModal) - Delete confirmation modal

### Data Management
- [`DataManager`](./global.html#DataManager) - Datapoint management
  - [`DataList`](./global.html#DataList) - Data list
  - [`DataItem`](./global.html#DataItem) - Data item
  - [`DataDetail`](./global.html#DataDetail) - Data detail
  - [`DataMenu`](./global.html#DataMenu) - Data menu
  - [`AddData`](./global.html#AddData) - Add data
- [`DeviceTree`](./global.html#DeviceTree) - Device tree
  - [`SearchDeviceTree`](./global.html#SearchDeviceTree) - Searchable device tree
  - [`TreeItem`](./global.html#TreeItem) - Tree item
  - [`TreeParent`](./global.html#TreeParent) - Tree parent node
- [`PropertySelector`](./global.html#PropertySelector) - Property selector
  - [`PropertyTable`](./global.html#PropertyTable) - Property table
  - [`PropertySelectTable`](./global.html#PropertySelectTable) - Property select table
  - [`ComputedPropertyConfig`](./global.html#ComputedPropertyConfig) - Computed property configuration

### Date & Time
- [`DatePicker`](./global.html#DatePicker) - Date picker
  - [`AggregationPicker`](./global.html#AggregationPicker) - Aggregation picker
  - [`WidgetDatePicker`](./global.html#WidgetDatePicker) - Widget date picker

### UI Components (Radix UI)
- **Button**
  - [`Button`](./global.html#Button) - Button component
  - [`buttonVariants`](./global.html#buttonVariants) - Button style variants
- **Dialog**
  - [`Dialog`](./global.html#Dialog), [`DialogTrigger`](./global.html#DialogTrigger), [`DialogContent`](./global.html#DialogContent)
  - [`DialogHeader`](./global.html#DialogHeader), [`DialogTitle`](./global.html#DialogTitle), [`DialogDescription`](./global.html#DialogDescription)
  - [`DialogFooter`](./global.html#DialogFooter), [`DialogClose`](./global.html#DialogClose)
  - [`DialogOverlay`](./global.html#DialogOverlay), [`DialogPortal`](./global.html#DialogPortal)
- **Dropdown Menu**
  - [`DropdownMenu`](./global.html#DropdownMenu), [`DropdownMenuTrigger`](./global.html#DropdownMenuTrigger), [`DropdownMenuContent`](./global.html#DropdownMenuContent)
  - [`DropdownMenuItem`](./global.html#DropdownMenuItem), [`DropdownMenuCheckboxItem`](./global.html#DropdownMenuCheckboxItem),
  - [`DropdownMenuShortcut`](./global.html#DropdownMenuShortcut)
  - [`DropdownMenuGroup`](./global.html#DropdownMenuGroup), [`DropdownMenuPortal`](./global.html#DropdownMenuPortal), [`DropdownMenuSub`](./global.html#DropdownMenuSub)
  - [`DropdownMenuRadioGroup`](./global.html#DropdownMenuRadioGroup)
- **Form**
  - [`Form`](./global.html#Form), [`FormItem`](./global.html#FormItem)
  - [`FormMessage`](./global.html#FormMessage), [`FormField`](./global.html#FormField)
- **Select**
  - [`Select`](./global.html#Select), [`SelectTrigger`](./global.html#SelectTrigger), [`SelectValue`](./global.html#SelectValue), [`SelectContent`](./global.html#SelectContent)
  - [`SelectItem`](./global.html#SelectItem), [`SelectGroup`](./global.html#SelectGroup), [`SelectLabel`](./global.html#SelectLabel)
- **Table**
  - [`Table`](./global.html#Table), [`TableHeader`](./global.html#TableHeader), [`TableBody`](./global.html#TableBody), [`TableFooter`](./global.html#TableFooter)
  - [`TableRow`](./global.html#TableRow), [`TableHead`](./global.html#TableHead), [`TableCell`](./global.html#TableCell), [`TableCaption`](./global.html#TableCaption)
- **Tabs**
  - [`Tabs`](./global.html#Tabs), [`TabsList`](./global.html#TabsList), [`TabsTrigger`](./global.html#TabsTrigger), [`TabsContent`](./global.html#TabsContent)
- **Card**
  - [`Card`](./global.html#Card), [`CardHeader`](./global.html#CardHeader), [`CardTitle`](./global.html#CardTitle), [`CardDescription`](./global.html#CardDescription)
  - [`CardContent`](./global.html#CardContent), [`CardFooter`](./global.html#CardFooter)
- **Accordion**
  - [`Accordion`](./global.html#Accordion), [`AccordionItem`](./global.html#AccordionItem), [`AccordionTrigger`](./global.html#AccordionTrigger), [`AccordionContent`](./global.html#AccordionContent)
- **Navigation Menu**
  - [`NavigationMenu`](./global.html#NavigationMenu), [`NavigationMenuList`](./global.html#NavigationMenuList), [`NavigationMenuItem`](./global.html#NavigationMenuItem)
  - [`NavigationMenuTrigger`](./global.html#NavigationMenuTrigger), [`NavigationMenuContent`](./global.html#NavigationMenuContent), [`NavigationMenuLink`](./global.html#NavigationMenuLink)
  - [`NavigationMenuIndicator`](./global.html#NavigationMenuIndicator), [`NavigationMenuViewport`](./global.html#NavigationMenuViewport)
  - [`navigationMenuTriggerStyle`](./global.html#navigationMenuTriggerStyle)
- **Carousel**
  - [`Carousel`](./global.html#Carousel), [`CarouselContent`](./global.html#CarouselContent), [`CarouselItem`](./global.html#CarouselItem)
  - [`CarouselPrevious`](./global.html#CarouselPrevious), [`CarouselNext`](./global.html#CarouselNext)
- **Toast**
  - [`Toast`](./global.html#Toast), [`ToastAction`](./global.html#ToastAction), [`ToastClose`](./global.html#ToastClose)
  - [`ToastTitle`](./global.html#ToastTitle), [`ToastDescription`](./global.html#ToastDescription), [`ToastViewport`](./global.html#ToastViewport)
  - [`Toaster`](./global.html#Toaster) - Toast container
- **Tooltip**
  - [`Tooltip`](./global.html#Tooltip), [`TooltipTrigger`](./global.html#TooltipTrigger), [`TooltipContent`](./global.html#TooltipContent)
- **Popover**
  - [`Popover`](./global.html#Popover), [`PopoverTrigger`](./global.html#PopoverTrigger), [`PopoverContent`](./global.html#PopoverContent)
- **Other UI**
  - [`Input`](./global.html#Input) - Input field
  - [`Textarea`](./global.html#Textarea) - Text area
  - [`Checkbox`](./global.html#Checkbox) - Checkbox
  - [`Switch`](./global.html#Switch) - Switch
  - [`RadioGroup`](./global.html#RadioGroup), [`RadioGroupItem`](./global.html#RadioGroupItem) - Radio group
  - [`Label`](./global.html#Label) - Label
  - [`Badge`](./global.html#Badge), [`badgeVariants`](./global.html#badgeVariants) - Badge
  - [`Calendar`](./global.html#Calendar) - Calendar
  - [`Separator`](./global.html#Separator) - Separator
  - [`ScrollArea`](./global.html#ScrollArea), [`ScrollBar`](./global.html#ScrollBar) - Scroll area
  - [`Status`](./global.html#Status) - Status indicator

### User Interface
- [`Login`](./global.html#Login) - Login page
  - [`LoginForm`](./global.html#LoginForm) - Login form
  - [`ForgotPassword`](./global.html#ForgotPassword) - Forgot password
- [`UserSetting`](./global.html#UserSetting) - User settings
  - [`UserInfoForm`](./global.html#UserInfoForm) - User info form
  - `PasswordChangeContent` - Password change

### Utility Components
- [`Loading`](./global.html#Loading) - Loading component
  - [`Loader`](./global.html#Loader) - Loader
  - [`LoadingDots`](./global.html#LoadingDots) - Loading dots
  - [`LoadingSpinner`](./global.html#LoadingSpinner) - Loading spinner
- [`EmptyState`](./global.html#EmptyState) - Empty state display
- [`FallbackUi`](./global.html#FallbackUi) - Fallback UI
- [`LazyLoader`](./global.html#LazyLoader) - Lazy loader
- [`MultiStepForm`](./global.html#MultiStepForm) - Multi-step form
  - [`StepperIndicator`](./global.html#StepperIndicator) - Stepper indicator
- [`NavigationTabs`](./global.html#NavigationTabs) - Navigation tabs
- [`NotFound`](./global.html#NotFound) - 404 page
- [`NotAuth`](./global.html#NotAuth) - Authentication failed page
- [`LastUpdated`](./global.html#LastUpdated) - Last updated time
- [`QuestionTooltip`](./global.html#QuestionTooltip) - Help tooltip
- [`CooldownButton`](./global.html#CooldownButton) - Cooldown button

## 🪝 Custom Hooks

### Authentication & API
- [`useAuth`](./global.html#useAuth) - Authentication state management
- [`useApi`](./global.html#useApi) - API client (inventory, events, measurements, alarms)

### UI & State
- [`useDark`](./global.html#useDark) - Dark mode
- [`useToast`](./global.html#useToast) - Toast notifications
- [`useBranding`](./global.html#useBranding) - Branding configuration
- [`useTranslation`](./global.html#useTranslation) - Internationalization

### Data Management
- [`useDeviceTree`](./global.html#useDeviceTree) - Device tree
- [`useDeviceInventory`](./global.html#useDeviceInventory) - Device inventory
- [`useVirtualTable`](./global.html#useVirtualTable) - Virtual scroll table
- [`useWidgetSize`](./global.html#useWidgetSize) - Widget size management
- [`useUltivisDeviceContext`](./global.html#useUltivisDeviceContext) - Ultivis device context
- [`useUltivisLogic`](./global.html#useUltivisLogic) - Ultivis business logic

### Navigation & Context
- [`useRoutingContext`](./global.html#useRoutingContext) (useRouting) - Routing context
- [`useInventoryContext`](./global.html#useInventoryContext) - Inventory context
- [`useTransitionNavigate`](./global.html#useTransitionNavigate) - Transition navigation

### Advanced Hooks
- [`useCustomMutation`](./global.html#useCustomMutation) - Custom mutation hook
- [`useIntersectionObserver`](./global.html#useIntersectionObserver) - Intersection Observer API hook
- [`useUpdatedConfig`](./global.html#useUpdatedConfig) - Updated configuration management
- [`useUpdateForTypeDashboard`](./global.html#useUpdateForTypeDashboard) - Type dashboard update

## 🎁 Providers

Context provider components:
- [`AuthProvider`](./global.html#AuthProvider) - Authentication context provider
- [`BrandingProvider`](./global.html#BrandingProvider) - Branding context provider
- [`DarkProvider`](./global.html#DarkProvider) - Dark mode context provider
- [`RoutingProvider`](./global.html#RoutingProvider) - Routing context provider
- [`UltivisDeviceProvider`](./global.html#UltivisDeviceProvider) - Ultivis device context provider

## 📦 State Stores

Zustand-based state management:
- [`useRoleStore`](./global.html#useRoleStore) - User roles and permissions management
- [`useUserAgentStore`](./global.html#useUserAgentStore) - User agent and device type detection

## 🗂️ Data & Constants

Ultivis IoT platform and application data schemas:

### Alarm Data
- Alarm severity levels (CRITICAL, MAJOR, MINOR, WARNING)
- Alarm status (ACTIVE, ACKNOWLEDGED, CLEARED)
- Alarm icon mapping

### Chart Data
- Chart types (Line, Bar, Pie, Gauge, etc.)
- Chart display options
- Chart color palettes

### Event Data
- Ultivis IoT event schema
- Event type definitions

### Font Data
- Font family options
- Font weights (100-900)

### Managed Objects
- Ultivis IoT device and asset schema
- Managed object property definitions

### Measurements
- Ultivis IoT measurement data schema
- Time-series data types

### Period Data
- Time interval options (5min, 1hour, 1day, etc.)
- Period selection presets
- Aggregation methods (MIN, MAX, AVG, etc.)

### Tenant Configuration
- Ultivis IoT tenant configuration schema
- Tenant property definitions

## 🎨 Styles & Theming

- TailwindCSS-based styling
- Dark mode support
- Customizable themes

## 🔧 Utilities

Helper functions and utilities:

### Styling & UI
- [`cn`](./global.html#cn) - Class name merging (TailwindCSS + clsx)

### Authentication
- `auth` - Authentication utility functions

### Data Processing
- `data` - Data processing and transformation utilities
- `property` - Property management and validation utilities

### Widget Management
- [`widgetManager`](./global.html#widgetManager) - Widget registration, configuration, and rendering management

### Internationalization
- `i18n` - Multi-language configuration and language switching
- [`humanizeAppName`](./global.html#humanizeAppName) - Convert app name to human-readable format