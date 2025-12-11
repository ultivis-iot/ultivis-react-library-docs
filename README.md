# Ultivis React Library

## 📦 Installation

```bash
npm install @ultivis-iot/react
# or
yarn add @ultivis-iot/react
```

## 🚀 Quick Start

### 1. AppProviders Setup (c8y Project)

```jsx
import { AppProviders } from '@ultivis-iot/react';
import { createBrowserRouter } from 'react-router-dom';
import '@ultivis-iot/react/styles';

const router = createBrowserRouter([
  // Route configuration
]);

function App() {
  return (
    <AppProviders
      router={router}
      favicon="/favicon.ico"
      brandLogo="/logo.png"
      navLogo="/nav-logo.png"
    />
  );
}

export default App;
```

### 2. Non-c8y Project Setup

For use in non-c8y environments:

```jsx
import { useState, useEffect } from 'react';
import { AppProviders, Login } from '@ultivis-iot/react';
import '@ultivis-iot/react/styles';

// Custom API implementation
const dashboardApi = {
  getDashboard: async (id) => {
    /* ... */
  },
  createDashboard: async (dashboard) => {
    /* ... */
  },
  updateDashboard: async (id, dashboard) => {
    /* ... */
  },
  deleteDashboard: async (id) => {
    /* ... */
  },
};

const userApi = {
  putCurrentUser: async (body) => {
    /* ... */
  },
  putPassword: async (newPassword, currentPassword) => {
    /* ... */
  },
};

function App() {
  const [isAuthenticated, setIsAuthenticated] = useState(false);

  if (!isAuthenticated) {
    return <Login onLogin={handleLogin} />;
  }

  return (
    <AppProviders
      router={router}
      c8yAuth={false}
      apis={{
        dashboard: dashboardApi, // For DynamicDashboard (optional)
        user: userApi, // For UserSetting (optional)
      }}
    />
  );
}
```

### 3. Layout Usage

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

- `Layout` - Main layout component (header, sidebar, content area)
- `Header` - Application header
  - `AppSwitcher` - App switcher
  - `AppSwitcherItem` - App switch item
  - `UserMenu` - User menu
  - `UserMenuItem` - User menu item
  - `HeaderDivider` - Header divider
- `Sidebar` - Sidebar navigation
  - `SidebarItem` - Sidebar menu item
  - `GroupAccordion` - Group accordion
  - `SidebarAccordionItem` - Sidebar accordion item
- `MenuBar` - Menu bar
  - `ActionItem` - Action item
  - `TabItem` - Tab item

### Form Fields

- `FormInputField` - Text input field
- `FormSelectField` - Select field
- `FormCheckboxField` - Checkbox field
- `FormSwitchField` - Switch field
- `FormRadioField` - Radio button field
- `FormTextareaField` - Textarea field
- `FormColorField` - Color picker field
- `FormIconSelectField` - Icon select field
- `FormInputArrayField` - Array input field
- `EditableField` - Editable field

### Dashboard

- `ContextDashboard` - Dynamic context dashboard
- `StaticDashboard` - Static dashboard
- `DashboardTabs` - Dashboard tabs
- Dashboard modals
  - `DashboardModal` - Dashboard settings modal
  - `WidgetModal` - Widget settings modal
  - `SelectWidget` - Widget selection
  - `Configuration` - Widget configuration
  - `PreviewWidget` - Widget preview
  - `RemoveModal` - Delete confirmation modal

### Data Management

- `DataManager` - Datapoint management
- `DeviceTree` - Device tree
- `SearchDeviceTree` - Searchable device tree
- `PropertySelector` - Property selector
- `ComputedPropertyConfig` - Computed property configuration
- `VirtualTable` - Virtual scroll table
- `ExpandableCell` - Expandable table cell

### Date & Time

- `DatePicker` - Date picker
- `WidgetDatePicker` - Widget date picker

### UI Components (Radix UI)

- **Button**
  - `Button` - Button component
  - `buttonVariants` - Button style variants
- **Sheet**
  - `Sheet`, `SheetTrigger`, `SheetContent`, `SheetClose`
  - `SheetHeader`, `SheetTitle`, `SheetDescription`
  - `SheetFooter`, `SheetPortal`, `SheetOverlay`
- **Dialog**
  - `Dialog`, `DialogTrigger`, `DialogContent`
  - `DialogHeader`, `DialogTitle`, `DialogDescription`
  - `DialogFooter`, `DialogClose`
  - `DialogOverlay`, `DialogPortal`
- **Dropdown Menu**
  - `DropdownMenu`, `DropdownMenuTrigger`, `DropdownMenuContent`
  - `DropdownMenuItem`, `DropdownMenuCheckboxItem`
  - `DropdownMenuShortcut`
  - `DropdownMenuGroup`, `DropdownMenuPortal`, `DropdownMenuSub`
  - `DropdownMenuRadioGroup`
- **Form**
  - `Form`, `FormItem`
  - `FormMessage`, `FormField`
- **Select**
  - `Select`, `SelectTrigger`, `SelectValue`, `SelectContent`
  - `SelectItem`, `SelectGroup`, `SelectLabel`
- **Table**
  - `Table`, `TableHeader`, `TableBody`, `TableFooter`
  - `TableRow`, `TableHead`, `TableCell`, `TableCaption`
- **Tabs**
  - `Tabs`, `TabsList`, `TabsTrigger`, `TabsContent`
- **Card**
  - `Card`, `CardHeader`, `CardTitle`, `CardDescription`
  - `CardContent`, `CardFooter`
- **Accordion**
  - `Accordion`, `AccordionItem`, `AccordionTrigger`, `AccordionContent`
- **Navigation Menu**
  - `NavigationMenu`, `NavigationMenuList`, `NavigationMenuItem`
  - `NavigationMenuTrigger`, `NavigationMenuContent`, `NavigationMenuLink`
  - `NavigationMenuIndicator`, `NavigationMenuViewport`
  - `navigationMenuTriggerStyle`
- **Carousel**
  - `Carousel`, `CarouselContent`, `CarouselItem`
  - `CarouselPrevious`, `CarouselNext`
- **Toast**
  - `Toast`, `ToastAction`, `ToastClose`
  - `ToastTitle`, `ToastDescription`, `ToastViewport`
  - `Toaster` - Toast container
- **Tooltip**
  - `Tooltip`, `TooltipTrigger`, `TooltipContent`
- **Popover**
  - `Popover`, `PopoverTrigger`, `PopoverContent`
- **Other UI**
  - `Input` - Input field
  - `Textarea` - Text area
  - `Checkbox` - Checkbox
  - `Switch` - Switch
  - `RadioGroup`, `RadioGroupItem` - Radio group
  - `Label` - Label
  - `Badge`, `badgeVariants` - Badge
  - `Calendar` - Calendar
  - `Separator` - Separator
  - `ScrollArea`, `ScrollBar` - Scroll area
  - `Status` - Status indicator

### User Interface

- `Login` - Login page
- `UserSetting` - User settings

### Utility Components

- `Loading` - Loading component
  - `LoadingDots` - Loading dots
  - `LoadingSpinner` - Loading spinner
- `EmptyState` - Empty state display
- `ConfirmDialog` - Confirmation dialog (custom message, icon, loading state support)
- `AppIcon` - Application icon component
- `FallbackUi` - Fallback UI
- `LazyLoader` - Lazy loading
- `MultiStepForm` - Multi-step form
  - `StepperIndicator` - Step indicator
- `NavigationTabs` - Navigation tabs
- `NotFound` - 404 page
- `NotAuth` - Authentication failure page
- `LastUpdated` - Last update time
- `QuestionTooltip` - Help tooltip
- `CooldownButton` - Cooldown button

## 🪝 Custom Hooks

### Authentication & API

- `useAuth` - Authentication state management
- `useApi` - API client (inventory, events, measurements, alarms)

### UI & State

- `useDark` - Dark mode
- `useToast` - Toast notifications
- `useBranding` - Branding settings
- `useTranslation` - Multi-language
- `useSidebarStore` - Sidebar state management (Zustand)
- `useSidebarContext` - Sidebar context

### Data Management

- `useDeviceTree` - Device tree
- `useDeviceInventory` - Device inventory
- `useVirtualTable` - Virtual scroll table
- `useWidgetSize` - Widget size management
- `useUltivisDeviceContext` - Ultivis device context
- `useUltivisLogic` - Ultivis business logic

### Navigation & Context

- `useRoutingContext` (useRouting) - Routing context
- `useInventoryContext` - Inventory context
- `useTransitionNavigate` - Transition navigation

### Advanced Hooks

- `useCustomMutation` - Custom mutation hook
- `useIntersectionObserver` - Intersection Observer API hook
- `useUpdatedConfig` - Updated configuration management
- `useUpdateForTypeDashboard` - Type dashboard update

## 🎁 Providers

Context provider components:

- `AuthProvider` - Authentication context provider
- `BrandingProvider` - Branding context provider
- `DarkProvider` - Dark mode context provider
- `RoutingProvider` - Routing context provider
- `UltivisDeviceProvider` - Ultivis device context provider

## 📦 State Stores

Zustand-based state management:

- `useRoleStore` - User role and permission management
- `useUserAgentStore` - User agent and device type detection

## 🗂️ Data & Constants

Ultivis IoT platform and application data schemas:

### Alarm Data

- Alarm severity levels (CRITICAL, MAJOR, MINOR, WARNING)
- Alarm status (ACTIVE, ACKNOWLEDGED, CLEARED)
- Alarm icon mapping

### Chart Data

- Chart types (Line, Bar, Pie, Gauge, etc.)
- Chart display options
- Chart color palette

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
- Time series data types

### Period Data

- Time interval options (5min, 1hour, 1day, etc.)
- Period selection presets
- Aggregation methods (MIN, MAX, AVG, etc.)

### Tenant Configuration

- Ultivis IoT tenant settings schema
- Tenant property definitions

## 🎨 Styles & Theming

- TailwindCSS-based styling
- Dark mode support
- Customizable themes

## 🔧 Utilities

Helper functions and utilities:

### Styling & UI

- `cn` - Class name merging (TailwindCSS + clsx)

### Authentication

- `auth` - Authentication utility functions

### Data Processing

- `data` - Data processing and transformation utilities
- `property` - Property management and validation utilities

### Widget Management

- `widgetManager` - Widget registration, configuration, rendering management

### Internationalization

- `i18n` - Multi-language settings and language switching
- `humanizeAppName` - Convert app name to human-readable format
