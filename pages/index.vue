<script setup lang="ts">

const incomes = [
{
	date: '01-11-2024',
	totalAmount: '$250.00',
	incomeName: 'Jobs',
},
  {
	date: '03-11-2024',
	totalAmount: '$150.00',
	incomeName: 'Gig',
  },
  {
	date: '07-11-2024',
	totalAmount: '$350.00',
	incomeName: 'Gift',
  },
]

const expenditures = [
  {
	date: new Date().toISOString().split('T')[0],
	totalAmount: '$250.00',
	expenditureName: 'Groceries',
  },
  {
	date: new Date().toISOString().split('T')[0],
	totalAmount: '$150.00',
	expenditureName: 'Gym',
  },
  {
	date: new Date().toISOString().split('T')[0],
	totalAmount: '$350.00',
	expenditureName: 'Delivery',
  },
  {
	date: new Date().toISOString().split('T')[0],
	totalAmount: '$550.00',
	expenditureName: 'Electronics',
  },
]

</script>

<template>
	<main class="container pt-8">
		<h2 class="mb-4">Budget dashboard</h2>

		<div class="grid gap-4 lg:grid-cols-2">
			<Card class="mb-4">
				<CardHeader>
					<CardTitle>Income</CardTitle>
				</CardHeader>
				<CardContent>
					<Table>
						<TableHeader>
							<TableRow>
								<TableHead class="w-[150px]">Date</TableHead>
								<TableHead>Name</TableHead>
								<TableHead class="text-right">Amount</TableHead>
							</TableRow>
						</TableHeader>
						<TableBody>
							<TableRow v-for="(item, index) in incomes" :key="index">
								<TableCell class="font-medium">{{ item.date }}</TableCell>
								<TableCell>{{ item.incomeName }}</TableCell>
								<TableCell class="text-right">{{ item.totalAmount }}</TableCell>
							</TableRow>
						</TableBody>
					</Table>
				</CardContent>
			</Card>

			<Card class="mb-4">
				<CardHeader>
					<CardTitle>Expenditure</CardTitle>
				</CardHeader>
				<CardContent>
					<Table>
						<TableHeader>
							<TableRow>
								<TableHead class="w-[150px]">Date</TableHead>
								<TableHead>Name</TableHead>
								<TableHead class="text-right">Amount</TableHead>
							</TableRow>
						</TableHeader>
						<TableBody>
							<TableRow v-for="(item, index) in expenditures" :key="index">
								<TableCell class="font-medium">{{ item.date }}</TableCell>
								<TableCell>{{ item.expenditureName }}</TableCell>
								<TableCell class="text-right">{{ item.totalAmount }}</TableCell>
							</TableRow>
						</TableBody>
					</Table>
				</CardContent>
			</Card>
		</div>
		
	</main>
</template>
